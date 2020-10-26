# Kenny Tilton's Road to Lisp

## When did you first try Lisp seriously?

1995 or '96. My initial interest in programming when I went shopping
for my first computer in 1977 was artificial intelligence, so of
course I heard about Lisp, and when I ran across a Lisp 1.5 Manual in
one geek shop I snagged it. But I could not make any sense out of it.

Fast forward five years and now I am a VAX/VMS consultant doing
business apps in tall buildings, and while reading some geek rag I am
stunned to see Lisp listed as a 4GL based on the 4GL definition of
being an order of magnitude more productive than a 3GL. This was
strange because 4GLs generally created (the illusion of) greater
productivity with screen builders and a super high level (hence
inflexible) language with database stuff done for you. And I knew Lisp
was not like that. But I just filed this data point away and went on
with my life.

Five more years later and I decide to write a program which could
check intermediate steps of arbitrary first-year high school algebra
problems, as part of a tutorial. I see Microsoft (!) offers a Logo,
and I remember the 4GL data point and decide what the hell, let's
learn a new language at the same time.

I loved it, and went amazingly far with Logo on the tutorial before
realizing it would have to be ported to "C" -- a most unpleasant
exercise. And it was then another ten years before I found my way out
of the desert and back to Lisp.

## Which Lisp did you try?

Common Lisp. Digitool's MCL, to be specific.

## What led you to try Lisp?

I was looking for A Better Way than "C" for version two of my algebra
tutorial application. I knew I wanted OO because I could see in my C
code that I was using structs in an OO kinda way. I also knew I wanted
a dynamic, interactive development environment. And it had to run on
the Mac, where I made most of my sales.

The first thing I tried was Stoney Ballard's Component Workshop, a
brave attempt at a dynamic C++. Never even got to "Hello world", then
Stoney gave up. When i got Symantec C++ (I had used it when it was
Michael Kahl's Think C) I freaked out when I saw incremental linking
was gone and every edit-run cycle now included a twenty second link
from scratch. Also I was just appalled by C++ the language.

Next up was SmalltalkAgents from Quasar Knowledge Systems. QKS kept
saying how great they were and how great they were going to
be. Perhaps, but not by crashing my Mac every five minutes.

I then announced on Compuserve's MACDEV forum that I was giving up and
was going to use C++, when a kind soul from Cambridge, Mass suggested
I look at MCL. He said it was compiled, fast, mature, object-oriented
and a few other things.

Well the amazing thing was that I had been skipping MCL ads in the
Apple Developer association catalog for months, because of my earlier
experience with Logo. I had no idea of the progress in Lisp compilers.

I also had come incredibly close when I got the pre-alpha Dylan CD
from Apple Computer and played with that. Dtlan was being developed
for Apple by Digitool, and it ran atop (ait for it) Macintosh Common
Lisp! Who knew?

But having read the message from Cambridge, I promptly ordered a copy
of MCL. It came a few days later, and just while assembling the manual
pages into a binder I concluded I had found The One. I gave the
install CD to my two developers, told them to dump QKS, then ordered
two more copies to stay honest.

The next few weeks involved everyone taking turns running to each
others' desk to show them neat new features we'd just discovered, and
I have never looked back.

## If you were trying Lisp out of unhappiness with another language, what was it and what did you not like about it, or what about Lisp were you hoping to find different?

I wanted a dynamic development modality, no linker especially. And an
end to pointers and dereferencing and manual memory management. ie, I
was looking for a better way than C, and when I looked at C++ I did
not find it.

## How far have you gotten in your study of Lisp? (I know, that is hard to measure)

Well, it's been seven years, so as an application developer I am
fluent.

## What do you think of Lisp so far?

Perfect. Whatever it does not do, macros let me coax from CL. Being
able to restart from a backtrace after hours of debugging (or while
trying twenty things a minute apart to get something working) is an
enormous win. CLOS is unspeakably powerful. A simple thing like
special variables is magnificent when you really need them. Of course
garbage collection is a stupendous win. The speed is crucial. Multiple
inheritance and multi-methods are vital.

One thing a lot of newbies experience, as did I, is that when I go to
find out how some function works, it always turns out to work just the
way I happen at that time to expect or want or need it to. Clearly
Common Lisp is the product of a long history of refinement by good
engineers with a strong ethic of doing things right.

And if you have to know, lawdy, i never want to edit without
parentheses again. When reworking code, the code tree is perfect for
moving chunks of semantics around. And the autoindentation is a
significant time saver. I refactor a lot, and thus a lot of time in
other languages goes into tediously realigning code.
