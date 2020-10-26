# Pete Kirkham

## When did you first try Lisp seriously, and which Lisp family member was it?

Earlier this year (2003).

## What led you to try Lisp?

I'd used it as an undergrad years ago, and various people on the
xml-dev mailing list either refer to lisp or to paul graham's
writings.

## Where did your road originate?

I've been growing increasingly annoyed by Java's verbosity as a
prototyping language, and that virtually every system i've worked I've
had to implement some form of expression evaluator.

In my day job I do a lot of prototyping of exploritory numerical
applications- the aim is to find a solution to a problem, and display
the results.I prototype in Java at the moment because it's easy to
knock up a GUI which plots the results of a calculation, and the
calculations are pretty fast (Hotspot JVMs blow away fortran for
math).

But I do find myself repeating the same idioms (generally at a
granularity that OO inheritance can't help with) and hand coding the
same optimisations (which I can't tell the compiler to do as it's
stupid).

Also the number of postings on comp.lang.java.developer that say 'how
to I write an expression evaluator' or 'why does Java not have a macro
language' made me think about getting somthing better.

## How far have you gotten in your study of Lisp?

I've read quite alot of basic stuff getting a better idea of how it's
all put together, and am putting together an implementation in Java of
a common lisp-related language that suits my needs (macros, iterative
development, access to Java's portable GUI libraries, all the tricks I
know for numerical optimisations built into the compiler, running on a
Hotspot JVM that optimises the native code based on runtime
profiling).

## What do you think of Lisp so far?

Cool. Terse. Small (compared to the Java APIs I'm used to). Hackable.
