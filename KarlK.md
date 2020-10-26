# Karl K

## When did you first try Lisp (meaning here and throughout the survey "any member of the Lisp family") seriously, and which Lisp family member was it?

I took summer computer science courses which used Scheme in 1992 and
1993 (via the Johns Hopkins CTY program -- hi Mark and Jeff, wherever
you are!). It was the first "real" language I used (for values of
"real" that do not include microcomputer BASIC or LOGO). The Scheme
flavor was EdScheme on small Macintoshes, a good way to learn the
value of tail-recursion as (fib 26) using naive recursion took more
than a day to compute.

I hadn't seriously used a Lisp since then -- taking the slow overland
route by way of Perl and Python.

Now (2003) I am studying Common Lisp on my own. I began chiefly with
CLISP but am now using mostly SBCL for its larger set of available
packages.

## What led you to try Lisp?

A number of things. I'd read some of Paul Graham's essays recently --
and while I am given to understand that he is not CL's biggest fan (or
perhaps that CLers are not his) he does convey very ably the reasons
to try any Lisp at all.

Also, I find it interesting to consider that other languages' feature
sets have tended more towards the Lispy as time has gone on -- vide
Python, in which I do most of my "work" programming. I do not agree
with the "messianic" view that I have seen some express -- that a
return to Lisp is inevitable -- since I suspect that the success of a
language in the modern world depends also on things such as open and
free standard libraries (where Python and Perl win over any particular
Lisp) as well as syntax -- but it would be nice if it happened.

Plus, it just seemed worth learning. I'm a Unix person; Unix people
use lots of languages. :)

## If you were trying Lisp out of unhappiness with another language, what was that other language and what did you not like about it, or what were you hoping to find different in Lisp?

I would not say that I am unhappy with Python. However, the Python
designers tend to be very opinionated about retaining minimal syntax,
because extra syntax means extra reserved words and a more complicated
parser. This seems backwards to me: new syntax options are a feature
and not a bug.  There have been some "blue sky" discussions about what
it would take to have Lisp-like macros in Python, but I do not think
it will happen.

## How far have you gotten in your study of Lisp? (I know, that is hard to measure)

I'm working on writing some simple utilities for myself in SBCL,
notably a network port scanner as my "real work" involves network
systems security.

## What do you think of Lisp so far?

Macros are great. It's interesting how the same sorts of operations
that in other languages become "idioms" -- which is to say, "typing
the same thing, over and over again" -- become simple utility macros
in Lisp.

CLOS is pretty impressive as well, now that I've mostly got my head
around the idea of multiple dispatch.

As I'm discovering more available libraries, I'm less convinced that
there is a real shortage of them (of course, I'm using Debian) and am
more concerned about the availability of documentation for
them. Perhaps I will write some up and send it to maintainers. :)
