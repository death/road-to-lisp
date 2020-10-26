# Thomas F Burdick

## When did you first try Lisp (meaning here and throughout the survey "any member of the Lisp family") seriously, and which Lisp family member was it?

I had dabbled a bit in Emacs Lisp, Scheme, and Common Lisp, but when I
tried Lisp seriously, it was Common Lisp, in 1999.

## What led you to try Lisp?

I was working on some hairy C++ code, and according to the profiler, I
needed to make it faster.  Constantly referring to the assembly
output, I rewrote the affected functions and got a significant speed
gain.  Unfortunately, the resulting code was impossible to follow, and
had what looked like an "obvious" bug (even I was tempted to "fix" it,
and I knew why it was there!).  So, I tried again, and rewrote the
code readably, but this time paying close attention to efficiency.
Now I had clear, maintainable code that *should* have been fast, but
for one problem -- gcc wouldn't give me as efficient code as I wanted.
I knew that the compiler should be free to make certain optimizations
on the code, but I had no way of communicating this to the compiler: I
had to choose between readability and optimizability.

My solution?  I figured that I needed a way to pass
promises/hints/transforms to the compiler.  I wanted to be able to
write my code for human beings, and provide the extra information the
compiler needed to transform it into more efficient code.  I was
already a big fan of Literate Programming, so this seemed like a
natural enough desire.  I got the gcc source code, and started hacking
at it, to give myself the tools I needed.  After some success on small
examples, I ran into a problem trying to implement what I needed for
the production code.  It seemed there was a bug in the gcc internals,
or maybe I just couldn't understand the code.  At this point, I turned
to a gcc guru I knew, and asked him if he could help me figure out
what was going on.

He was (in retrospect, justifiably) horrified.  He pointed out that no
one would want to use my custom, hacked C++ compiler, and that I was
working hard against the C++ way of doing things.  He told me that I
should look at Lisp, which is a language that explicitly supports what
I was trying to do: its macros are really program-transformations, and
it has compiler-macros that are almost exactly what I was (badly)
reinventing.

I decided to learn Lisp for real, especially this new world of macros.
Skipping past all the cute recursion/closures stuff filling up the
beginnings of Lisp books, I picked up Paul Graham's *On Lisp,* and
jumped straight to Chapter 7, "Macros".

## If you were trying Lisp out of unhappiness with another language, what was that other language and what did you not like about it, or what were you hoping to find different in Lisp?

C++ promised abstraction, and efficiency, but it could only deliver on
one at a time.  I wanted to be able to write custom transforms, and
generally assist the compiler, so my abstract, readable code would
turn into well-tuned machine code.

## How far have you gotten in your study of Lisp? (I know, that is hard to measure)

I've gotten quite good at working with Python (the CMUCL/SBCL
compiler) to get the machine code I want, from my readable source
code.  I'm a good, competent applications programmer, and I've worked
some in implementation.  I still learn things all the time (this is a
good thing to me).

## What do you think of Lisp so far?

I love it!  I still learn new languages, but the desperate search for
Something Better is gone.  I'm happy using it.  I may later discover
new Holy Grails that I need to search for, but for now, I've found
mine: I can copy pseudo-code out of notes, or papers, and build the
Lisp system up to the point where it can run it; not only run the
pseudo-code, but do so efficiently.
