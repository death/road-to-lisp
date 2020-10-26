# Peter Housel

## When did you first try Lisp (meaning here and throughout the survey "any member of the Lisp family") seriously, and which Lisp family member was it?

My first exposure to Lisp was in 1981 as a first-year high school
student, reading the first edition of Artificial Intelligence by
Winston and Horn.  Later when I was a second- or third-year
high-schooler, the Lisp half of the book was split out into a separate
book, which I bought and read religiously.  Unfortunately my computer
at the time (a TRS-80 with a 2MHz Z-80 processor, 48K of RAM and no
disk drives) wasn't powerful enough to run a decent Lisp.

During my fourth year of high school, I acquired a copy of The Revised
Maclisp Manual (the PITMANUAL) and started on a project to implement
MACLISP in Motorola 68000 assembly language.  This project got
sidetracked while I started to implement my own assembler and
machine-language monitor, and eventually fell by the wayside.  I did
become intimately familiar with MACLISP, however, though I was never
actually able to run it.

During my first year of college, I [ported the Franz Lisp
interpreter](http://www.mit.edu/afs/athena/astaff/reference/4.3network2/usr.bin/lisp/Notes.tahoe)
included with BSD 4.3 Unix from the VAX to the CCI Tahoe architecture.
The Tahoe performed at about six times the speed of a VAX 11/780, and
architecture was very similar to the VAX with some gratuitous
differences.  Franz Lisp in those days was not written for
portability; even the C code used lots of `asm("...")` statements, and
the build relied on a tool to modify the generated assembly code to
globally allocate some registers.  By the middle of my second year of
college (the end of 1986), I had managed to port the compiler (named
"liszt") also, and eventually my port made it onto the BSD 4.3-Tahoe
software release.

The Franz Lisp developed within UC Berkeley was a dialect of MACLISP.
The commercial Franz Lisp was beginning to support Common Lisp by that
time, but the BSD version never got any of that code.

## What led you to try Lisp?

It was largely my interest in AI, initially sparked by reading Douglas
Hofstadter's Gödel, Escher, Bach: an Eternal Golden Braid.  By the
time I graduated, though, my interest had shifted more towards
language implementation, due to both AI winter and my experiences
porting Lisp and Pascal compilers.

## If you were trying Lisp out of unhappiness with another language, what was that other language and what did you not like about it, or what were you hoping to find different in Lisp?

For an electrical engineering student and part-time Unix system
administrator/programmer, languages such as C, Fortran and MATLAB
proved much more practial than Lisp for anything but AI class
projects.  However, I found myself wishing for a Lisp-based extension
language to escape the boring details of explicit memory management in
C.  Once you've known garbage collection other dynamic features, it's
hard to go back.

To be continued...

## How far have you gotten in your study of Lisp? (I know, that is hard to measure)

## What do you think of Lisp so far?
