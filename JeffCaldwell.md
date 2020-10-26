# Jeff Caldwell

I wrote this in December, 2002. Since then, I have written a lot more
Lisp code. When I read this now, much of it gives me the "Ah,
grasshopper!" feeling. There were things I didn't know, or things that
have changed since. However, not enough time has passed for me to
revise the article. Perhaps in a year or two I will be very interested
in writing about all the things I have learned since I wrote this
original record of my discovery of Lisp.  For now, I will say that I
remain amazed every day at how easily I can build powerful
programs. Programming is fun again.

## Learning Lisp

posted by Jeff on Tuesday December 31, @04:55AM

from the **why-bother** dept.

Nobody uses Lisp. All those parenthesis? It's a dead language. It's
not for real work. Just some eggheads use it. Why bother? It turns out
that maybe there are some reasons...

Over the past year I began reading about Lisp. Then I began learning
Lisp, and programming in Lisp. I am still learning and have a lot left
before I will have hit my limit. In this article I discuss how I came
to discover Lisp and why I chose some of the Lisp tools I am
using. There are lots of links for you to use to discover Lisp on your
own.

People seem to have strong, and wrong, preconceived notions about
Lisp. Here's what I like about Lisp:

- It is incremental.
- Lisp can compile one function at a time, even as it is typed. Of
  course, Lisp can handle files or entire systems of files as a group,
  too.
- Suppose I have a running program, whether it is a running Windows or
  GUI program, or a web server, or anything at all. If I change a
  function, the new function takes effect immediately, as soon as I
  type in the change. I don't have to stop and restart the
  program. The change picks up in the middle of the running
  program. (I can load only the one function or reload the entire file
  of functions.)
- It is multiprocessing. Most Lisp implementations provide full
  support for multiprocessing, threads, and so on.
- It is interactive. Lisp gives me a Read-Evaluate-Print Loop, or a
  REPL. Lisp comes up in an initial state, ready to run, and presents
  me with a command prompt. It reads the command I type, evaluates
  that command, and prints the result. Lisp then waits to read my next
  command. I can issue the command to launch a GUI or webserver. The
  REPL prompt returns and I can then interact with the running program
  by examining or setting variables, changing functions, setting
  breakpoints, and much more.
- It is flexible. Where do I begin here? There is so much flexibility,
  I cannot explain it in one paragraph. Those who defined Lisp took a
  long, hard look at many, or even most, of the basic issues involved
  in language design and provided mechanisms for Lisp to do it, not
  one of those ways, but all of those ways. Lisp has both dynamic and
  lexical scope, both local and global environments, named and unnamed
  functions. Every language lets you write code that is executed at
  run time. Lisp allows you to write code that is executed at compile
  time; macros can, during the compile, read code you've written and
  manipulate it to generate new code, which then is compiled. Lisp
  functions behave as regular functions and as data. Assign an
  existing function to a new function name. Change the original
  function to do some bookkeeping work and then call the original
  function. All of that without changing the source code for the
  original function. This goes on and on, I cannot fit it all in
  here. As John Foderaro said, Lisp is a programmable programming
  language.
- From Peter Norvig's *Paradigms of Artificial Intelligence
  Programming*:
  - Built-in Support for Lists
  - Automatic Storage Management
  - Dynamic Typing
  - First-Class Functions
  - Uniform Syntax
  - Interactive Environment
  - Extensibility
  - History
- Lisp is fast. Nearly all modern Lisps compile to native machine
  code. I have written prime number algorithms, taken from [Knuth
  Volume II](http://www-cs-faculty.stanford.edu/~knuth/), that run
  about as fast as equivalent C programs. This is not unusual. Look at
  [Edi Weitz's benchmarks](http://weitz.de/cl-ppcre/) of his portable
  Common Lisp regular expression code. He benchmarked his Lisp code
  against Perl's regular expressions. Guess which was faster? (And
  Perl is known for its regular expressions.)
- Lisp has many datatypes, not just lists. Arrays, hashes, structures,
  strings, and then all of the Common Lisp Object System, are
  included.
- It is concise.
- All those parenthesis. You know, it's odd that what seemed so
  foreign and repeling at the beginning is something I now appreciate
  deeply. The parenthesis would be unusable if it were not for modern
  editors. These editors perform indentation based upon the
  parenthetical level and so make things visually apparent. The
  editors also highlight matching open/close pairs. So what? Why have
  them in the first place? The reason is that Lisp has almost no
  syntax at all. An open parenthesis means "the next token is a
  function to be called". All tokens after the first one are
  parameters to the function. The close parenthesis means "end of the
  parameters". The net effect is that, when I write a new function, it
  is called in exactly the same way that in-built functions such as
  **if**, **+**, and so on are called. There is no difference. In
  essence, when I define a new function, I have extended Lisp
  itself. In fact, most in-built Lisp functions are defined in
  Lisp. Ultimately, there are maybe 25 "raw Lisp" special operators
  that cannot be defined without "outside help". All of that is
  possible only because of the parenthesis! (Of course, one could
  argue for the use of other special characters, but so what? That
  would not be anything new, really. See the next topic.)
- Reader macros exist. Every program, function or variable that Lisp
  reads, whether interactively or in batch, passes through the Lisp
  reader. Lisp allows the reader to be modified by the use of reader
  macros. A reader macro recognizes an input pattern that is not part
  of "pre-defined Lisp" and translates that pattern into something
  that "traditional Lisp" recognizes. This means that the use of
  reader macros changes the syntax of the Lisp that you type.
- It is functional. In other words, it is built out of functions,
  where a function causes no side effects but returns a value. That
  value can be data or another function. Functions are first-class,
  which means they can be passed around like data. You can write code
  with side effects, and often need to do that. But you can write
  functional code when that is the right thing to do. Most often, it
  is the right thing to do.
- It supports recursion well. In many languages, a recursive call is
  performed by slapping yet another marker onto the stack and going
  through a procedure call. This approach is limited by the stack
  size, in terms of space, and the time required for a procedure call
  and return, in terms of time. *Tail recursion* is possible when the
  current invocation of the function is complete at the time the
  recursive call is made. In other words, the current invocation is
  not waiting on the recusive call to return before the current
  invocation can complete its calculations. When a compiler (or
  interpreter) recognizes tail recursion, the compiler can turn the
  recursion into a loop. This avoids the space and time overhead. Tail
  recursion is fast. For many algorithms, a recursive implementation
  is beautiful and easy to understand, when compared to a procedural
  implementation. Most Lisp compilers support tail recursion and so
  permit writing code that is beautiful to the person and fast for the
  machine.

Lots of languages have some of these pieces. I'm not sure of any other
language that has all of them. It used to be that Lisp was the only
language in this category, and that is beginning to change. However, I
am unaware of any language I can point to and say "That is Lisp all
over again". To my knowlege, Lisp still stands alone.

My interest in Lisp began when I read [Structure and Interpretation of
Computer
Programs](http://mitpress.mit.edu/sicp/full-text/book/book.html)
(available online), commonly called *SICP* or *The Wizard Book*
(because of its cover). This is an amazing computer science textbook
with an incredible worldwide reputation. The book opened my eyes in
many ways. SICP uses a Lisp dialect called
[Scheme](http://www.schemers.org/), which prides itself on an
as-simple-as-possible structure. Scheme and the ideas in SICP were a
perfect meld. SICP uses math-oriented topics to present computer
science ideas during the first chapter. (The math isn't too heavy but
I want math-phobic people to have a little warning.) The math lets up
after that but the computer science is unrelentingly beautiful.

I did not continue working with Scheme after I finished SICP. I didn't
find any implementations that gave me easy GUI or web
development. (Not that I searched very hard, though, it just didn't
occur to me to do so.) I had no good replacement for a Unix bash
shell. I kind of thought "That was an interesting language for
learning all those computer science topics." and that was about it.

All that began to change, though, when I read [Kent Pitman's slashdot
interview](http://interviews.slashdot.org/article.pl?sid=01/11/03/1726251&mode=thread&tid=156). (Kent's
response was longer than slashdot prefers. They split his response and
the second half is
[here](http://interviews.slashdot.org/article.pl?sid=01/11/13/0420226&mode=thread&tid=156).

Mr. Pitman was involved in ANSI committees standardizing Lisp. His
article, which actually consists of responses to questions, rekindled
my interest in the Lisp language family and, in particular, gave me a
reason to consider Common Lisp in addition to Scheme. The entire
definition of Scheme is shorter than the table of contents for the
definition of Common Lisp. This apparently delights Schemers. Common
Lisp is designed to be industrial strength.

I still was not actively learning Lisp. It was just something
interesting and it seemed much more worthwhile than before. It had
moved from obscure and arcane to having real potential. A few months
later, I ran across the [slashdot
story](http://developers.slashdot.org/article.pl?sid=02/02/02/1917202&mode=thread&tid=156)
about [Paul Graham](http://www.paulgraham.com/)'s book [On
Lisp](http://www.paulgraham.com/onlisp.html) being available
online. It was an easy decision to download a copy. I also grabbed a
free copy of Common Lisp.

(Look on [Paul Graham's Lisp
page](http://www.paulgraham.com/lisps.html). [CMU Common
Lisp](http://cons.org/cmucl/) is free for
Unix/Linux. [CLisp](http://cons.org/cmucl/) runs on more platforms,
including Windows. [Corman Lisp](http://www.cormanlisp.com/) runs only
on Windows, has a free download, a trial period for its IDE, is built
as an in-process COM server, and allows "straight Win32 SDK programs
to be built". The Corman site also has a [free download of
PowerLisp](http://www.cormanlisp.com/PowerLisp.html) for the
Mac. Other commercial versions include [Franz's *Allegro Common
Lisp*](http://www.franz.com/) and [Xanaly's
*Lispworks*](http://www.lispworks.com/).)

I personally use Lispworks Professional Edition on Windows and look
forward to purchasing it for Linux. Lispworks has a wonderful CAPI
package for building GUIs portable between Windows and Linux. CAPI is
very nice for many, or even most, tasks. I suspect, though, that if
you really need super-tight Windows integration, Corman Lisp may be
worth a look. Allegro is out of my current price range, especially
since Lispworks allows free run-time distribution and Allegro requires
a license purchase for every run-time station. I currently run CMUCL
on Linux. I need to take a closer look at CLisp and Corman.

I worked through every example in *On Lisp* and was totally jazzed by
the power of the language. I became convinced. I bought lots of other
Lisp books, including [Peter Norvig](http://norvig.com/)'s [Paradigms
of Artificial Intelligence Programming](http://norvig.com/paip.html),
which is tremendously worthwhile and is about much more than just
Artificial Intelligence. I read Sonia Keene's [Object-Oriented
Programming in Common Lisp - A Programmer's Guide to
CLOS](http://www.amazon.com/exec/obidos/tg/detail/-/0201175894/qid=1041333127/sr=8-1/ref=sr_8_1/104-7327602-1790358?v=glance&s=books&n=507846)
(Addison Wesley) for the object-oriented aspects of Common Lisp. Paul
Graham's [Ansi Common
Lisp](http://www.amazon.com/exec/obidos/tg/detail/-/0133708756/qid=1041333218/sr=1-1/ref=sr_1_1/104-7327602-1790358?v=glance&s=books)
is good as a look-it-up handbook, especially when struggling to learn
all the Common Lisp functions. [Christian
Queinnec's](http://videoc.lip6.fr/queinnec/WWW/Queinnec.html) [Lisp In
Small
Pieces](http://www.amazon.com/exec/obidos/ASIN/0521562473/qid%3D1041333253/sr%3D11-1/ref%3Dsr%5F11%5F1/104-7327602-1790358)
is breathtaking. It is what I am reading currently. It does what it
says and defines Lisp in terms of Lisp by starting small and then
adding a piece at a time. Three chapters of this book have done more
to increase my understanding of some formerly-esoteric, but frequently
bumped-into, features of Lisp than all the previous books had managed
to do. I suppose that's just part of the learning process. (*Lisp In
Small Pieces* is not a good introduction to the language -- One
Amazon.com review calls it "graduate or advanced undergraduate". Read
the book later, but certainly read it.) I have other books in my
stack. I'm looking forward to [The Art of the MetaObject
Protocol](http://www.amazon.com/exec/obidos/tg/detail/-/0262610744/qid=1041334296/sr=8-1/ref=sr_8_1/104-0178778-4207945?v=glance&s=books&n=507846),
to learn about peering inside Common Lisp Object System, or CLOS,
objects. I've got a scattering of other books, which I'll post more
about as I get to them.

[Cliki](http://www.cliki.net/index) is a great place to learn and to
find resources. You can get a lot of nice free tools at [Franz's Open
Source page](http://opensource.franz.com/). There are a variety of web
servers available.

For my purposes, I am currently working with the
[Apache](http://www.apache.org/) web server and two tools from
[OnShore Development](http://www.onshored.com/): [1) IMHO and 2)
UncommonSQL](http://alpha.onshored.com/lisp-software/). IMHO is a
CLOS-based set of tools for presenting web pages and retrieving
responses, including state management. IMHO interfaces to the Apache
httpd using mod_webapp. UncommonSQL allows access to databases,
specifically Oracle, using OCI calls, and Postgres.

I evaluated lots of other systems before deciding upon my current
configuration. (See [Cliki](http://www.cliki.net/index) for links.)
Web servers such as PortableAServe, an open source version of
AllegroServe from Franz, don't separate code from data well enough for
my liking. In other words, the application itself it tightly
intertwined with the html. To a possibly-large extent, the same may be
true of the large and wonderful CL-HTTP from MIT. CL-HTTP has two or
three problems. Many people don't like its license and so steer clear
of it. I am not a lawyer and don't want to have to consult one before
comitting to a course of action. I mean, I don't need to consult one
if I simply make another choice where the license is clear. I had no
trouble getting CL-HTTP working under Windows with Lispworks. I don't
have Lispworks for Linux and so tried getting CL-HTTP working on Linux
with CMUCL. I never really succeeded. After thinking about the
licensing issues and the configuration problems I had, which probably
were entirely my own fault, I took a look at the CL-HTTP code. It
seems to me that it, too, mixes the application with the HTML in
much-too-tight a way. I really was looking for a clean separation, in
part because of the application design I have in mind.

IMHO and UncommonSQL seem to give me that separation. IMHO defines the
web interactions as a series of operations on CLOS
objects. UncommonSQL defines database transactions similarly. I'm just
getting started here so whatever I have misunderstood will become
clear in a few weeks and months. My current understanding is that I
will be able to define macros and/or CLOS objects above and around the
IMHO and UnCommonSQL objects, thus giving me an object-oriented system
controlling both the database and the web server. I can add
functionality to control, or produce, whatever else I need.

I am truly enjoying my experience with Lisp. Perhaps you will take a
similar journey.
