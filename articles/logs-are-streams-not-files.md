---
author: Adam Wiggins
source: http://adam.herokuapp.com/past/2011/4/1/logs_are_streams_not_files/
---

<h1>Logs Are Streams, Not Files</h1>

<p>Server daemons (such as PostgreSQL or Nginx) and applications (such as a Rails or Django app) sometimes offer a configuration parameter for a path to the program’s logfile. This can lead us to think of logs as files.</p>

<p>But a better conceptual model is to treat logs as time-ordered streams: there is no beginning or end, but rather an ongoing, collated collection of events which we may wish to view in realtime as they happen (e.g. via <code>tail -f</code> or <code>heroku logs --tail</code>) or which we may wish to search in some time window (e.g. via <code>grep</code> or Splunk).</p>

<h2>Using the power of unix for logs</h2>

<p>Unix provides some excellent tools for handling streams. There are two default output streams, <code>stdout</code> and <code>stderr</code>, available automatically to all programs. Streams can be turned into files with a redirect operator, but they can also be channeled in more powerful ways, such as splitting the streams to multiple locations or pipelining the stream to another program for further processing.</p>

<p>A program that uses <code>stdout</code> for its logging can easily log to any file you wish:</p>

<pre><code>$ mydaemon &gt;&gt; /var/log/mydaemon.log</code></pre>

<p>(Typically you would not invoke this command directly, but would run this from an init program such as Upstart or Systemd.)</p>

<p>Programs that send their logs directly to a logfile lose all the power and flexibility of unix streams. What’s worse is that they end up reinventing some of these capabilities, badly. How many programs end up re-writing log rotation, for example?</p>

<h2>Distributed logging with syslog</h2>

<p>Logging on any reasonably large distributed system will generally end up using the syslog protocol to send logs from many components to a single location. Programs that treat logs as files are now on the wrong path: if they wisht to log to syslog, each program needs to implement syslog internally - and provide yet more logging configuration options to set the various syslog fields.</p>

<p>A program using <code>stdout</code> for logging can use syslog without needing to implement any syslog awareness into the program, by piping to the standard <code>logger</code> command available on all modern unixes:</p>

<pre><code>$ mydaemon | logger</code></pre>

<p>Perhaps we want to split the stream and log to a local file as well as syslog:</p>

<pre><code>$ mydaemon | tee /var/log/mydaemon.log | logger</code></pre>

<p>A program which uses <code>stdout</code> is equipped to log in a variety of ways without adding any weight to its codebase or configuration format.</p>

<h2>Other distributed logging protocols</h2>

<p>Syslog is an entrenched standard for distributed logging, but there are other, more modern options as well. <a href="http://www.splunk.com/">Splunk</a>, fast becoming a indispensable tool for anyone running a large software service, can accept syslog; but it also has its own custom protocol which offers additional features like authentication and encryption. <a href="https://github.com/facebook/scribe/wiki">Scribe</a> is another example of a modern logging protocol.</p>

<p>Programs that log to <code>stdout</code> can be adapted to work with a new protocol without needing to modify the program. Simply pipe the program’s output to a receiving daemon just as you would with the <code>logger</code> program for syslog. Treating your logs as streams is a form of <a href="http://en.wikipedia.org/wiki/Future_proof">future-proofing</a> for your application.</p>

<h2>Logging in the Ruby world</h2>

<p>Most Rack frameworks (Sinatra, Ramaze, etc) and Rack webservers (Mongrel, Thin, etc) do the right thing: they log to <code>stdout</code>. If you run them in the foreground, as is typical of development mode, you see the output right in your terminal. This is exactly what you want. If you run in production mode, you can redirect the output to a file, to syslog, to both, or to any other logging system that can accept an input stream.</p>

<p>Unfortunately, Rails stands out as a major exception to this simple principle. It creates its own log directory and writes various files into it; some plugins even take it upon themselves to write their own, separate logfiles. This hurts the local development experience: what you see in your terminal isn’t complete, so you have to open a separate window with <code>tail -f log/*.log</code> to get the information you want. But it hurts the deployment experience even more, because you end up having to tinker around with a bunch of Rails logger configuration options to get your logs from all your web machines to merge into a single stream.</p>

<h2>Logging on Heroku</h2>

<p>The need to treat application logs as a stream is especially poignant with <a href="http://blog.heroku.com/archives/2010/12/13/logging/">Heroku's new logging system</a>. On the backend, we route logs with a syslog router written in Erlang called <a href="https://github.com/heroku/logplex">Logplex</a>.</p>

<p>Logplex handles input streams (which we call “sinks”) from many different sources: all the dynos running on the app, system components like our HTTP router, and (currently in alpha) logs from add-on providers. Sinks are merged together into channels (each app has its own channel) which is a unified stream of all logs relevant to the app. This allows developers to see a holistic view of everything happening with their app, or to filter down to logs from a particular type of sink (for example: just logs from the HTTP router, or just logs from worker processes).</p>

<p>Further, log streams can also be sent outbound, which we call “drains.” Users can configure syslog drains, and we’re currently working up a technical design for how add-on providers can automatically add drains. This latter item will enable a new class of log search and archival add-on, most notably the emerging syslog-as-a-service products like <a href="http://www.loggly.com/">Loggly</a> and <a href="https://papertrailapp.com/">Papertrail</a>.</p>

<p>This logging system works quite well, and it gets even better with the new features on the way - but it only works where all programs output their logs as streams. Programs that write logfiles, such as Rails in its default configuration, don’t make sense in this world.</p>

<p>As a workaround, Heroku injects the <a href="https://github.com/ddollar/rails_log_stdout/blob/master/init.rb">rails_log_stdout</a> plugin into Rails apps at deploy time. We’d prefer not to have to do this (injecting code is a dicey way to solve problems), but it’s the best way to get Rails logs into the app’s logstream without requiring extra configuration from the app developer.</p>

<h2>Conclusion</h2>

<p>Logs are a stream, and it behooves everyone to treat them as such. Your programs should log to <code>stdout</code> and/or <code>stderr</code> and omit any attempt to handle log paths, log rotation, or sending logs over the syslog protocol. Directing where the program’s log stream goes can be left up to the runtime container: a local terminal or IDE (in development environments), an Upstart / Systemd launch script (in traditional hosting environments), or a system like Logplex/Heroku (in a platform environment).</p>

