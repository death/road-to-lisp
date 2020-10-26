# Tomer Altman

## When did you first try Lisp seriously, and which Lisp family member was it?

Meaning any member of the Lisp family. As for "when", many of us had
multiple encounters with a Lisp before it really stuck. The "stick"
date is of most interest.

I first encountered it in Richard Fateman's CS 61a course at UC
Berkeley, which is based off of Brian Harvey's adaptation of MIT's
SICP-based course (Spring 2000). I liked it, had fun, but for variousr
reasons ( "it's slow! No one uses it!", etc. ), I never really used it
for a long time...

Then, I was working on a research project, using C, and I was getting
nowhere fast. I tried Prolog as an alternative, and then I considered
using Scheme, since as a member of the Lisp family of languages, it
should be adept at symbolic tasks. It worked! The benefits of Scheme (
weakly-typed, encouraged abstraction, interpreter-debugging, etc. )
allowed me to fix bugs, clean up code, and achieve 3 years of C code
in three months. That was the summer of 2003. Then, I leaned that
Scheme ( & Lisp in general ) are pretty much the only Very High-Level
Languages (VHLLs) which have high-quality compilers. Why would I use
any other "scripting language", no matter how popular it is, when I
can get an order of magnitude speed-up? There's simply no
comparison...

## What led you to try Lisp?

Well, I needed a high-level solution to my research problem ( as
Greenspun predicted, I re-invented half of Prolog in C to solve my
problem! ).

## What other languages have you been using most?

C for "application" programming, PHP/Perl for web-scripting ( I hate
Perl for web-scripting now ), Octave/Maxima for numerical & symbolic
scientific computing...

## How far have you gotten in your study of Lisp?

Hard to answer, I know. Just looking for a rough idea.

Well, one thing that I like about Lisp/Scheme is that once you
*really* understand it, you can implement it yourself from scratch! I
cannot think of a single other computer language that one can say that
about... most "popular" languages are not democratic like that; they
are benign dictatorships. So in pursuit of that, I'm re-reading ( and
now *understanding* ) SICP, learning Common Lisp syntax, and using CL
to fully understand macros via Paul Graham's "On Lisp". I am beginning
to understand macros in principle. I need to finish the book,
though. To further my depth of understanding of the language vs. the
implementation, I'm implementing a Scheme in a non-Lispy
VHLL. Hmmm... what else? I use HOF's plentifully in my code, and I'm
trying to write libraries to contribute to the Scheme Library.

## What do you think of Lisp so far?

I love it! I feel now that I can do anything! C really depressed me as
a programmer. Everything felt hard!

Also, as a scientist, I hate things which are ad hoc; I want to
understand the systematic principles that order things. In that
regard, Lisp is great; you can understand it at every level. Perl,
Python, etc. are just glorious hacks that approximate the features
Lisp had already in the 1960's. They're messy and all their end-users
just worship the sole implementator(s) as programming deities, and
they rarely understand what is under the hood.

In another reserach project that I worked on in the summer of 2003, my
collaborator wanted to program it in C++. So I reluctantly learned
C++. I liked it relative to C, but there was one thing that I began to
notice. With C++, you have to keep *so* many things in your mind at a
time! It is a language full of exceptions, special cases, and a slew
of features. It really slowed down my coding, because I had my nose in
a syntax book all the time. Also, it took 10x as long to compile
relative to C. With Scheme, it is so curt & elegant in its design,
that I rarely find myself looking up esoteric syntax
situations. Someone once said that people-cycles are more expensive
than CPU cycles. Well, I also think that we humans have a limited
amount of room in our "buffer" to keep all the language details in
mind all the time. With C++, I could never bear all the details in
mind all the time. With Scheme, it's a breeze.
