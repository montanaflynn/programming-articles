---
author: C. Lawrence Wenham
source: http://www.yacoset.com/Home/signs-that-you-re-a-good-programmer
---

### Signs that you're a good programmer

The most frequently viewed page on this site is [Signs you're a bad programmer](http://www.yacoset.com/Home/signs-that-you-re-a-bad-programmer), which has also now been published on dead trees by [Hacker Monthly](http://hackermonthly.com/issue-24.html), and I think that behoves me to write its antithesis. "Bad programmer" is also considered inflammatory by some who think I'm speaking down to them. Not so; it was personal catharsis from an author who exhibited many of those problems himself. And what I think made the article popular was the "remedies"--I didn't want someone to get depressed when they recognized themselves, I wanted to be constructive.

Therefore if you think you're missing any of the qualities below, don't be offended. I didn't pick these up for a while, either, and many of them came from watching other programmers or reading their code

### 1\. The instinct to experiment first

The compiler and runtime can often answer a question faster than a human can. Rather than seek out a senior programmer and ask them "will it work if I do this?", a good programmer will just _try it_ and see if it works before bringing their problem to someone else

#### Symptoms

1.  Side projects
2.  Dabbling in other programming languages, especially ones from a different "family" (procedural, stack-based, concurrent, etc.)
3.  Knows what you're talking about when you mention "Arduino"
4.  Old, uncommitted code that duplicates other code's functionality but isn't referenced elsewhere in the project
5.  A tendency to suggest wacky and unrealistic solutions in meetings
6.  A cubicle or desk populated with toys that came from ThinkGeek

#### How to acquire this trait

Are you excessively cautious? Are you only comfortable when you have permission? Has anyone ever said that you were passive aggressive? You might consider inviting some friends to visit the local Six Flags or some other roller-coaster park. If you want baptism by fire, then make your first ride the scariest (for me, it was the "[Drop Zone](http://www.themeparkreview.com/photos/kingsdominion/dropzone.htm)" at King's Dominion, with some reinforcement a few years later on the [Kingda Ka](http://www.sixflags.com/greatAdventure/rides/Kingdaka.aspx) at Six Flags). If you consider yourself ready to get off the kiddie rides you might try your hand at hang gliding and windsurfing, which have the benefit of teaching you what you can and cannot control

Much of what makes people timid to experiment is chemical--your brain has a small number of adrenergic receptors, so a little bit of adrenaline excites your fight-or-flight reflexes too much. But consider why people grow tolerant to coffee: the caffeine's byproducts force their brain to grow more adenosine receptors. So if you force your brain to grow more adrenaline receptors then the same amount of "fear juice" will trigger a lower percentage of them. Find some experience that scares the shit out of you, do it a few times, and you will lose your fear of venture on a physical level

**Note:** A programmer who "suggests wacky and unrealistic solutions" is not always a bad programmer. It can be a sign of creative thinking from someone who assumes confirmation or correction will come from somewhere else down the line.

### 2\. Emotional detachment from code and design

Code is like kleenex: you use it when it's useful and throw it away when it no longer serves. We all like to think that _code-reuse_ is important, and while it is, it's not meant to be about raising a child. Code doesn't feel. Code doesn't care. Code will turn on you like a Frankenstein monster. Code is just bytes. Code is a liability

#### Symptoms

1.  Almost no committed code that is commented out
2.  Willingly throws away weeks or months of work in order to adopt another programmer's superior code
3.  Puts finger to lips, furrows brow and says "hmm" when faults in their work are pointed out, _while looking at the code and not the critic_
4.  Indifferent to the way the IDE wants to auto-format code, uninterested in "tabs-vs-spaces" arguments
5.  Refers to it as "_the_ code" rather than "_my_ code", unless accepting blame
6.  Has abandoned a design of theirs that was previously used in a successful product
7.  Doesn't become defensive when the boss mentions that they're looking for an off-the-shelf alternative to what they've been writing for the past few years

#### How to acquire this trait

Konrad Lorenz, the author of _[On Aggression](http://www.amazon.com/gp/product/0156687410/ref=as_li_ss_tl?ie=UTF8&tag=synesmedia-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=0156687410)_, suggested that a scientist should begin each day by throwing out one of his pet theories in order to remain sharp. Consider throwing out one of your pet algorithms or design patterns or exquisite one-line Sodoku solvers every morning to remind yourself that it's you who controls the idea, not the idea that controls you

Find the code that you're the most proud of and delete it, now re-write it from scratch in a different way. Use a "design pattern" that confuses you, or that you _hate_ (e.g.: the Singleton) and figure out how to make it work. If necessary, delete that after you've got it working and try again with a new pattern or language. Not only will you learn that there's More Than One Way To Do It, but you'll learn that your code is transitory. Code, by its nature, is not just inextricably glued to its language, platform, and the APIs it consumes, but written in the form of ephemeral static charges, orientations of magnetic particles, subject to the whims of the market, Moore's Law, and your employer

Other techniques to break the abusive relationship

1.  Maintain somebody else's code
2.  Experience, either by accident or bloody intention, what it's like to lose a week's work to a failed backup or a botched commit and have to re-write it all over again
3.  Work for start-ups where you'll get laid-off when the second or third round of financing doesn't come through
4.  Be stupid enough to post your best code on Reddit
5.  Read the bit about "Destructive pursuit of perfection" further down in this article

### 3\. Eager to fix what isn't broken

Programs are infrastructure: they're built to serve a specific need, but **[needs always change](http://www.yacoset.com/Home/why-nobody-knows-what-they-are-doing)**. Good programmers realize that hard-coded values buried in code are bad, that a [destoryBaghdad() function is immoral](http://www.linfo.org/q_programming.html), and that it's a priority to eliminate "code smells". Not for pride. Not for backslapping attaboys from your peers or the authors of methodology books. But because **you will itch until it is fixed**

#### Symptoms

1.  Doesn't take the spec by its word and tries to find out who wrote it and what they were thinking
2.  Hunts down and talks to the people who will use the program each day
3.  Owns a book written by a guy called [Martin Fowler](http://www.amazon.com/gp/product/0201485672/ref=as_li_ss_tl?ie=UTF8&tag=synesmedia-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=0201485672)
4.  Tends to express _extreme like_ or _dislike_ for popular technologies such as XML, ORM and REST, and has also **switched positions** on one or more of these in the past
5.  Likes to use abstraction layers, but doesn't like to add more than one layer on top of what's already in the language or platform
6.  Talks about "low cohesion"
7.  At least 10% or more of their commits reduce the line-count of the project without adding new functionality
8.  Before adding a new feature, checks to see if an existing one can be re-designed to perform both tasks or replaced entirely with a better method

#### How to acquire this trait

The first attempt to solve a program in code will always bear the artifacts of discovery: discovering the true nature of the problem, discovering the features of the platform, and discovering the best way to solve it. The second attempt will be more stable, but might inherit too much cautionary baggage and become a nightmare to extend. And so many programs today are like the [Firth of Forth Bridge](http://en.wikipedia.org/wiki/Forth_Bridge): disgustingly over-engineered. Sometimes it's the developer's first crack at the problem and looks like a lawn mowed by a dog, sometimes it's their second attempt and looks like the dog installed grass-cutting laser turrets every 2 feet. It can take a third try before the designer understands the problem completely and knows how much, or how _little_ they need to do

Code lets you learn in stages where you don't need to re-write everything from scratch. You re-write pieces after you understand what they need to do and what they'll never need to do, make them simpler, shorter and beautiful

Go through your home and repair all the annoying things you've been putting off; fix the crooked picture on the wall, unclog the slow draining sink, repair that gutter drainpipe so your basement doesn't flood, buy a UPS and backup drive for your computer and configure them to shut-down/back-up automatically, replace all the incandescents with efficient bulbs, replace that ethernet cable draped down the hallway with WiFi or some proper wall-jacks and conduit, get a real food-dish for your cat instead of that old cheese-dip container

Next you should go to your last project and read through the code. Think about what each piece does. There's a loop here, some sorting there, a bit of number crunching, screen updates, HTML generation, database CRUD, that sort of thing

Now replace the hard-coded HTML with a templating system, get the database CRUD out of your business objects and re-write it to use proper parameterized queries instead of string concatenation, replace all the "writelns" and "MessageBoxes" in your error handlers with a logging framework, refactor code that's trying to borrow methods from other classes, use locale-aware string formatting, stop guessing how big an array should be and use a dynamic collection, delete orphaned code

Aim for these, in increasing order of importance

1.  Code that does the same thing, but is shorter or more efficient
2.  Code that does the same thing, but uses an appropriate "wheel" built-into the platform instead of reinventing its own
3.  Code that does the same thing, but is easier to modify for similar needs
4.  Code that does the same thing, but is easier to read and understand
5.  Code that doesn't exist

Hit #5 and you can call yourself a Zen Apprentice. Do it for a decade until you do it instinctively and you can call yourself a Zen Master


### 4\. Fascinated by the incomprehensible

I am only just beginning to understand what a Fourier Transform does, but I've been studying them because I have the _damn persistent feeling_ that I could be using them somehow. I don't know what I would use them for yet, but maybe I will someday. What I do know is that _what I don't know will cost me in useless labor_.

#### Symptoms

1.  Visits [Lambda The Ultimate](http://lambda-the-ultimate.org/) on a regular basis
2.  Knows what ATP synthase is. Has extracted DNA from a banana in their kitchen
3.  Owns a book with a [dragon on the cover](http://www.amazon.com/gp/product/0321486811/ref=as_li_ss_tl?ie=UTF8&tag=synesmedia-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=0321486811), especially if they don't write compilers
4.  Giggles when someone says the phrase "This is recorded on sticky-tape and rust"
5.  Shoves through a crowd at a party to get near someone who just used the word "Bayesian"
6.  Buys drinks for people who work in other industries and seem willing to talk shop when drunk
7.  Has a habit of boring people to tears explaining something tangentially related to the news, such as the cockpit layout of the Airbus 330
8.  Has foreign-language versions of popular songs on their iPod
9.  Envies but doesn't resent people with degrees in something they don't know

#### How to acquire this trait

This tends to start in childhood but can be cultivated in adulthood if you can commit to exploring your horizons. Friends are a major gateway: seek social occasions where you'll bump into people you don't know under circumstances where they'll be unhurried and at ease. This may involve alcohol. Don't try to impress them, don't compete with them, but display your ignorance willingly to see if they lean forward to correct and enlighten you. Then shut your fool trap and _listen_

When you hear or read something you don't recognize then Google it or hit Wikipedia. For a programmer an equally superior resource is [Ward Cunningham's Wiki](http://c2.com/cgi/wiki), which deserves weeks of your life

Computer programming has annexed all of the sciences and the feedback loop is so wide it stuns gods. From biology we took Genetic Algorithms. From climatology we took chaos theory. Biologists now use our work to fold proteins. Climatologists now use our simulations to predict armageddon. Everything informs us, and we inform everything. Either probe the unfathomable or retire on a "blub" programmer's salary.

### 5\. Compelled to teach

I once knew someone who thought it was good advice to "never teach everything you know" because they once lost a job after bringing a co-worker up to speed with all their skills. I stared at them with genuine incomprehension. A good manager would never get rid of someone who's not only capable of all their tasks but also demonstrates ability to train new workers. It would be like shooting the goose that lays golden eggs. If you get fired, it's probably for some other reason

#### Symptoms

1.  Blogs about their work
2.  Has an active Wikipedia account
3.  Unhesitant to pick up a marker and approach a whiteboard
4.  Commits changes to the repository that consist only of comments
5.  Lets new hires borrow books that cost them $100 to buy
6.  Pauses "[The Andromeda Strain](http://en.wikipedia.org/wiki/The_Andromeda_Strain_(film))" at the part about the sliver of paper getting between the bell and the ringer and grins like a madman

#### How to acquire this trait

I can only do this when I'm inspired or "in the mood", and I think that this mood is a product of circumstance, one that's made up of confidence, space, opportunity and provocation. When you're in school your teacher has the space and opportunity already supplied for them and their confidence is hopefully given by their training, but the _inspiration_ is tricky; it's the difference between a good lesson that both the teacher and the student enjoys and a laborious exercise in rote memorization

Novices in computer programming aren't usually novices in general, because they have lives and friends and family and hobbies and interests that have been going on for even longer. Maybe you do need to bore someone to tears by explaining something that's cool to you, even if it has nothing to do with programming. Maybe you have a younger sibling you can teach the guitar, or your favorite recipe, or how to balance on a pogo stick. Maybe you have a coworker who doesn't know how to ski. It doesn't matter the subject, just that you get a taste of what it's like to program someone else's brain in a positive way

If you've never taught anything before you will discover, to an embarrassing degree, just how many times you can say "um" and "er" per minute, how badly you're prepared, and how easily you can forget that the student doesn't know details you haven't explained yet

One of the tricks that worked for me was to volunteer for an opportunity to teach a complex subject (microbiology) to laymen. The first time I tried it I used a Post-It easel and a bunch of markers and tried to draw everything. I was all over the place. It was humiliating. But the audience, fortunately, was friendly

The next year I tried again, but this time I had an iPad and used Keynote to put together a presentation, which was a lot of fun in itself, but this time the lesson went overwhelmingly more smoothly. I used lots of pictures, very little text, almost no bullet points, a handful of jokes, and just relied on my memory to talk about slides I had designed to provoke my memory more than illustrate anything to the audience

The experience of doing an awful job the first time _informed_ my next attempt, and now that I've done it three or four more times I find I'm getting slightly better. Not only that, I now know ten times more about the subject because I studied like crazy to help temper my fear of being asked a difficult question. Teaching teaches the teacher

## Signs that you're a fantastic programmer

I only wish I had these traits and I can only write about them because I've observed them in others. Every now and then I have a moment where I think I'm living one of these, but those moments are rare and cherished. They are also debilitating and brush up against the stereotypes of autistic savants, trading one kind of virtue for another: if you want greatness you have to be prepared to pay

### 1\. Incorruptible patience

#### Symptoms

1.  Fire alarms provoke annoyance more than panic
2.  Cannot name any song that just played on the radio or through their headphones
3.  Is oblivious to how many times their cubicle-mate has gone for coffee, the bathroom, or the hospital
4.  Unbothered by office politics
5.  Can predict a bug before the code is ever run

#### How to acquire this trait

Distractions are a product of imagination. The day I wrote this I found myself horribly distracted and annoyed by someone at my gym singing songs in French while I sat in the sauna. The singing moved around outside the sauna and pissed me off. I wished he'd stop because I couldn't concentrate. I pictured a man without concern of others, a douchebag, someone who'd wear a pink shirt and order people around. Then I came out of the sauna and saw it was an old man, chocolate in complexion and as threatening as a worn teddy bear with button eyes. He'd started singing <u>La Vie en rose</u>, which is a song I that I not only loved but that made me wonder, just then, if it was me who'd long since turned into an insufferable asshole

I don't know how to shut out distractions, but if I had to try I'd guess it'd involve a little bit of deference and so much fascination that it directs your imagination instead of being dictated by it. When I want to be like this I want to take life without taking it personally

### 2\. A destructive pursuit of perfection

The worst optimizations favor profit over beauty, and between the two it's beauty that lasts longer. Perfection isn't the same as obsession, but they're damn close

#### Symptoms

1.  Preference for dismissal over compromise
2.  Contempt for delivery dates
3.  Substantial refactoring on the eve of a deadline
4.  Unwilling to accept bonuses, promotion, or stock options for expediency
5.  Fondness for films directed by Stanley Kubrick

#### How to acquire this trait

As [Tyler Durden says](http://www.amazon.com/gp/product/B001992NUQ/ref=as_li_ss_tl?ie=UTF8&tag=synesmedia-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=B001992NUQ) you must _know_--not _fear_--_know_ that someday you will die. Your nice condo with Ikea furniture is a side effect, not a reward. If you are not a unique, beautiful snowflake then what you create _has to be_.

It's also known as pride in one's work. Remember that emotional detachment from _code_ is a virtue, but this doesn't mean emotional detachment from your _work_ is, too. In fact, another way to become emotionally detached from _code_ is to put your interest into the _outcome_ instead. The outcome you should be thinking of is a lady who's going to get fired if she doesn't deliver the output of your program at 4:59pm sharp

There's a legend about a marketing type who worked for Sam Walton at Wal-Mart and came up with a brilliant campaign to advertise a widget. Sam took a look at the proposal and said something to the effect of "this is great, now take the cost of the campaign and use it to lower the price of the widget instead." According to legend, the widget sold better and made more profit that way than if the campaign had been carried out.

Let the spirit of the story roll around in your head for a while and think about how it'd map to what you do at work. You boss probably isn't like Sam Walton, but perhaps there's a little bit of Sam in you. Is it better to compromise the way others want, or to make the product just a little bit better

This could be hazardous to your income, it's risky to your stock options, but when you do a job _right_, when you do things _properly_, when you complete a project the way it _ought to be_, then sometimes time absolves all indulgences. Sometimes the boss calls you back to the carpet to apologize to _you_

### 3\. Encyclopedic grasp of the platform

Most programmers realize the short lifespan of their tools and don't waste much of their lives memorizing what's doomed to be obsolete. But neither do most programmers appreciate how everything in this industry is a derivative of some earlier thing, sharing syntax and constraints that will live well past our own personal expiration dates. The best programmers have done what Oxford used to insist on: if you learn latin and mathematics then you can fuck all of that other modern nonsense, because you'll have the tools you need to understand _anything_

#### Symptoms

1.  Can recite from memory all of the includables in the C Standard Library
2.  Raises a knowing eyebrow when you mention the "500 mile email"
3.  Has a copy of the OpenDoc Programmer's Guide gathering dust on their shelf
4.  Can complete any sequence of dialogue from Lord of the Rings, Star Wars, Red Dwarf or Monty Python
5.  Rapidly identifies a synchronization bug caused by TCP's Sliding Window algorithm
6.  Recognizes a bug that's caused by a microcode error on the CPU you're testing on
7.  Has a framed personal check for $2.56 from Donald Knuth

#### How to acquire this trait

Encyclopedic knowledge takes decades to acquire, but every Guru in the world got there by doing roughly the same three things each day

1.  Struggling to solve problems they find to be difficult
2.  Writing about how they solved difficult problems
3.  Reflecting on how they solved difficult problems

Once upon a time a novice programmer was stumped by a bug that he couldn't figure out. The crash report was full of strange numbers he didn't recognize, like -32,760\. Where the hell is that coming from? He hits Ctrl-F and searches all of his code files for "-32760" but it doesn't appear anywhere. Nothing makes any sense. A week goes past during which he goes back to his old college computer-science textbooks, the compiler's manual, everything, and on the last day his glazed eyes rest on a table of numbers. Through the fog of his tired mind he suddenly recognizes one of them: -32,76**8**. He thinks about how remarkable it is that it's so similar to his problem number, and then he notices that this table of numbers is showing the ranges for various integer types and how there can be _signed_ and _unsigned_ versions of both. When the light comes on it's blinding

Thrilled with his belated insight he writes a blog post about it which disappears into the global ether unread by all but a handful of buddies. That night he lies awake, thinking about that bug and about integer types and the pros and cons of compiler-checked types and so-on

Ten years later our friend is the lead programmer at the firm, and one day he glances over the shoulder of a junior programmer who's showing evident frustration. Tucked down in the stdout window is a bunch of debugging traces and the number -32,762\. The now-guru programmer taps the newbie on the shoulder and says "are you passing an _unsigned_ int16 to code that's expecting a _signed_ int16?

If you're not encountering problems that are difficult for you to solve then you need a change of job or hobby or scenery or something. Look for opportunities to work with something new at your job or school, try hacking your Roomba, pick a bug in an open-source project that nobody has touched for months and fix it, try answering tumbleweed questions on [StackOverflow](http://stackoverflow.com/) that force you to look up something you didn't know

If you could look inside the brain of a guru with a magic magnifying glass you might see clusters of neurons packed around the visual cortex that, like the infamous "[Grandmother cells](http://en.wikipedia.org/wiki/Grandmother_cell)", lie dormant for months but light up when something significant comes into view such as a power of two, or a suspiciously precise delay that points to a DNS timeout, or the signature of the [FDIV bug](http://en.wikipedia.org/wiki/Pentium_FDIV_bug). Those "grandmother cells" can only be made the hard way

### 4\. Thinks In Code

#### Symptoms

1.  In casual conversation their readiest metaphors come from programming constructs
2.  Spends the majority of their time "goofing off", but commits more bug-free code each day than their colleagues
3.  Glances over your shoulder and points at a bug in your code with their finger
4.  Correctly diagnoses bugs over the phone while drunk or in bed
5.  Comes up with their best code while taking a shower*
6.  When confronted with an obstinate bug, their instinct is to get up and go for a walk
7.  They suddenly pause and stare into space in the middle of a conversation, then abandon you to hurry back to their terminal with no explanation (AKA "A Columbo Moment" or "Gregory House behavior")

#### How to acquire this trait

Them darn kids and their cell phones, how does a 12 year-old teenage girl tap text messages on a numeric keypad so fast anyway? It can't be genetic, since all those damn brats can do it, no matter their gender or parentage. It can't be upbringing, cuz kids in every social class can do it. So you rule out this and that and what you're left with is an ancient truth: people think in the language they learned to speak. A teenager's thumbs already know where to go and they _think_ in texting. When writing, typos _feel wrong._ People who learn multiple spoken languages and use them regularly tend to think in multiple languages, too, after they've practiced for so long that they no longer have to do a translation in their heads first. Rather than read a phrase in Russian and translate it to English in their minds before understanding it, they just understand it in Russian.

You cannot think "_Fire rearward missile_" and then translate it to Russian, you **must think in Russian**

If you've heard about Sapir-Whorf or read _Nineteen Eighty Four_ and all that jazz then you might already appreciate the implications: words convey ideas, language _is_ thought. Whether that's a syntactic language or a visual or auditory language in your head doesn't matter, it's the way your brain deals with symbols and their rules for manipulation that matter

The best book you can read (and perform the exercises of) to acquire this trait is [Structure and Interpretation of Computer Programs](http://www.amazon.com/gp/product/0070004846/ref=as_li_ss_tl?ie=UTF8&tag=synesmedia-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=0070004846) by Abelson, Sussman and Sussman. It uses Scheme to present its lessons, and even if that's not the language you write programs in it's still one of the best languages to program your brain with. Remember: learn math and latin and you can understand _anything_

Whether you have this book or not the key is to practice with coding until you can read and reason with it like your native tongue. You can't acquire this trick in 30 days, it may be more like 30 months. You'll know if you've got it when you begin to _see in code_ as well.

<font size="1">* - Shaddap Bob, and you too, Sat.</font

### 5\. When In Rome, Does As Romans Do

I don't think I live up to this because I like to use [MonoTouch to write iOS apps](http://spentbetter.com/). I do know Objective-C and can write apps in it, but my heart belongs to LINQ. If I were to suppose an exception to this rule, it would be: "**but when in the Roman accounting department, does as accountants do**." It is not always wrong to pick a language that fits the domain, even if there's a performance or feature disadvantage from running in an interpreter or other layer. Yet great programmers will never insulate themselves from the hardware and will learn the native language anyway. [Every abstraction leaks](http://www.joelonsoftware.com/articles/LeakyAbstractions.html)

#### Symptoms

1.  No automatic interest in cross-platform frameworks
2.  Contemptuous of "language wars"
3.  Doesn't see a strategic disadvantage in maintaining the same program in multiple languages
4.  Assumes their own code is the source of a bug before blaming the compiler, library or operating system
5.  Displays a plush Tux penguin or Android in their cubicle soon after being assigned to a project targeting that platform
6.  Switches brand of cell phone or tablet in the same circumstance
7.  Hits a stack of technical manuals before assuming a data-type like _double_ or _decimal_ will do what they think on a new device

#### How to acquire this trait

These guys are as comfortable with platform diversity as they are with having multiple vegetables on the same dinner plate. I said "thinking in code" and "emotional detachment" were virtues, and this is the bonus that comes for free. While these programmers appreciate abstraction they don't automatically appreciate generalization. If there was no advantage to be had in a new platform, then why was it ever created

There's a thousand computer languages because there's a thousand classes of problems we can solve with software. In the 1980s, after the Macintosh debut, a hundred DOS products were ported to the new mouse-driven platform by clubbing the Alto-inspired UI over the head and brute-forcing the keyboard-driven paradigms of PCs into the Mac's visual atmosphere. Most of these were rejected by Apple or the market, and if they came back for a second try they came back because somebody flipped open the spiral-bound HIG and read it sincerely.

Maybe Excel needed to emulate Lotus 1-2-3's slash-driven menus. Maybe AutoCAD still needs to host a command line. But the designers of both never neglected the new world and that's why they're still famous today. Objective-C has Categories, C# has Extensions, but they're not quite alike and they're not quite the same. What's a Key-Value Observer to one might be like an Event to the other, which is as informative as saying an opportunity is the same as permission

To acquire this trait you have to begin by learning a new platform through both its unique instructions and _the way the user interacts with it_. Much of what's out there is made to be very similar to what you already know so you can start using it quickly (radically different platforms "ahead of their time" tend to fail), but be attentive to what's different. Android phones tend to include more hardware buttons than iPhones. Maybe that's good, maybe that's not, but their users _expect_ programs to use them. Don't disappoint them: neurons are harder to program than transistors

New platforms either debut a new language or new _conventions_ that are unique, and at whatever level that is you need to learn a new vocabulary. Even if it looks like they took an existing platform and "tweaked" it, the tweak in question must have significance. They say a Big Mac's Special Sauce is just Thousand Island dressing with more sweet pickle

To manage a single product written to multiple platforms you need to abstract _your_ product, not the platform its delivered to. You do that through elimination, by stripping platform-specific code out of your product's soul. If you can master "Eager to fix what isn't broken" then go bonkers on your code until there's only a few chunks left on the coroner's table; that's the part that stays.

The simpler it is, the easier to modularize. The easier to modularize, the easier to separate concerns. The easier to separate concerns, the less has to change to fix bugs and add features. The less has to change, the easier to translate those changes to another system. Don't rely on automatic methods--it's like relying on a cat to tie your shoelaces

### 6\. Creates their own tools

Symptoms

1.  Has set up an automated build server
2.  Has written their own benchmark or specialized profiler
3.  Maintains an open-source project on GitHub
4.  Has re-invented LISP at least once
5.  Knows what a Domain Specific Language is, and has designed and written an interpreter for one
6.  Extends their IDE/Editor with custom macros
7.  There's a Radio Shack project enclosure on their desk with a bunch of 7-segment displays showing the number of issues assigned to them in the bug tracker

## Signs that you're destined for more

These are not always the traits of "good" programmers, they're the traits of people who go beyond programming and change industries, some of them are even detrimental to what an employer would consider "good". If any of the following fits you then you should start your own company. I can't say if it'll benefit you to squander a few years in the bowels of a corporate beast to "learn the ropes", because if you exhibit these traits then I doubt it will be worth it. You are Steve Jobs or Bill Gates or their successors, and there's no way to learn these traits either because if you don't have them, then you ain't ever gonna.  

### 1\. Indifferent to Hierarchy

Richard Feynman once pointed out that "it doesn't matter who your dad knows", if something is wrong then it's wrong no matter who says its right. Don't fear the consequences to your career, you''ll find another job. Society never wastes real talent.  

#### Symptoms

1.  Getting into arguments with the CEO
2.  Quitting on principle
3.  Organizing teams without permission
4.  Creating new products after-hours while hiding from the Rent-a-Cops
5.  Re-organizing the workspace "Peopleware" style, against company policy
6.  Helps themselves to the boss's private stash of bottled water

### 2\. Excited by failure

Most of us learn from failure, but most of us also fear it. Even fewer of us have so much faith in their innate ability to cope and adapt that failure is actually seductive to them, and they must tempt more. They don't deliberately try to fail, they just _feel_ instinctively that failure can be as beneficial to them as it was to [Spencer Silver](http://www.todayifoundout.com/index.php/2011/11/post-it-notes-were-invented-by-accident/)

#### Symptoms

1.  Can tell you, step-by-step, what happened on United 232, Air France 447, March 28th 1979, or April 26 1986, and what changed as a result
2.  Snapped up an HP Touchpad when they went on sale for $100
3.  Took broken appliances apart as a kid, did not necessarily fix them
4.  Has tried every pick-up line there is and has the slap-marks on his cheeks to prove it
5.  Owns schwag from Dr. Koop, Enron, Pets.Com, excite, RIM and Yahoo!
6.  Founded a second start-up with the essence of their first start-up's failure

### 3\. Indifferent to circumstances

"The mind is its own place, and in itself can make a heaven of hell, a hell of heaven.

#### Symptoms

1.  Has transitioned from rags to riches to rags and shows no sign of regret to the latter
2.  Little or no loyalty to physical location or local traditions
3.  Disinterested by the outcome of elections
4.  Stock options and bonuses are ineffective retainment techniques
5.  Makes the best damn PB&J you've ever tasted, can prepare ramen sous-vide style with a ziplock bag and a space heater
6.  Cashes-in their 401k to fund their next venture

### 4\. Unswayed by obligations

Obligations are a social construct, and some see them as props for the lazy. While that's a dishonest oversimplification, some make it a point to break free and do something different. We'd still be bashing rocks together if they didn't

#### Symptoms

1.  Routinely applies for an extension to file taxes
2.  Antagonistic when asked to maintain code for "backwards-compatability"
3.  Contemptuous of Girl Scout Cookie order forms left out in the break room
4.  Dropped out of high-school, university, law or medical school because they didn't see the point anymore
5.  Has deeply religious parents but doesn't attend church
6.  Uses the free return-address envelope stickers given out by a cancer charity, frowns when you ask how much they gave

### 5\. Substitutes impulse for commitment

Companies are formed to 1: reduce the cost of a transaction, and 2: provide customer support. Our stereotypical "free spirit" isn't very good at the last one, but that's why they sell their stock to The Suits and fly away to build another nest

#### Symptoms

1.  Forgets Mother's Day/Valentine's Day/Anniversary but swamps the beloved with overcompensatory gifts shortly afterward
2.  Tends to give gifts that came from the SkyMall catalog
3.  Dedicates books/product launches/office buildings to close persons who didn't show-up for the ceremony
4.  Recruits a steadier person to run day-to-day operations

### 6\. Driven by experiences

The biggest programming challenges are still unknown; they're not quite the same as solving P=NP and more like figuring out how to get your customer laid. So somebody reacts boric acid and silicon oil, and that's nice, but it took a toy shop owner to turn it into _Silly Putty_

#### Symptoms

1.  Shows you a birds-eye photo of a woodland creek. When you shrug, they explain that it was taken on the return bounce
2.  Has opinions on the best parts of the Adirondack Trail
3.  Shows up at work with welts all over their arms, says it had something to do with a company called "Airsoft"
4.  Has eaten Ikizukuri or Fugu
5.  Laughs knowingly at the "strawberry cough" scene in [Children of Men](http://www.amazon.com/gp/product/B001YV502C/ref=as_li_ss_tl?ie=UTF8&tag=synesmedia-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=B001YV502C)

**N.B.**: While the toy-shop owner figured out that Silly Putty could be a toy, it took someone who was already $12K in debt to survive the silicone shortages of the Korean War before becoming rich. Not even the most inspired programmers, inventors, or entrepreneurs live in a vacuum. Someone invents it, another figures out what to do with it, and somebody else figures how to turn it into a business. Just look at the gadget you're using to read this article

## Further Reading

*   [The Programmer Competency Matrix](http://www.indiangeek.net/wp-content/uploads/Programmer%20competency%20matrix.htm)

## Credits

Thanks to [Mark Martino](http://www.seanet.com/~marmar/index.html) for reading an early draft of this article and providing ideas
