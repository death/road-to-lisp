# Ralph Richard Cook

## When did you first try Lisp (meaning here and throughout the survey "any member of the Lisp family") seriously, and which Lisp family member was it?

I first tried Lisp as an undergrad at Georgia Tech in the early
'80s. More recently I started up with Common Lisp this year (2003).

## What led you to try Lisp?

## If you were trying Lisp out of unhappiness with another language, what was that other language and what did you not like about it, or what were you hoping to find different in Lisp?

Back in the early '80s I was a CS student at Georgia Tech, and had
some Lisp courses, and like most everyone I thought "Ick!
Parentheses!" and forgot about it for a while. I went through the
usual '80s and '90s stuff, doing Windows programming in C and C++,
later moving on to Java, then Python. Along the way I read the Gang of
Four's Design Patterns book and saw how CLOS with multimethods got rid
of the need for the Visitor pattern. Interesting.

In the past couple of years I've gotten interested in functional
programming, which first took me through Scheme and Lisp, looking at
SICP and my old Lisp textbooks, but again I thought "Ick!
Parentheses!".

I then looked at Haskell since it's a pure functional
language. Problem is, it's a pure functional language, and as most
people here know sometimes imperative is better for some things, such
as multiplying matrices but mainly for I/O. Haskell's monads made my
head hurt. Sometimes you just want to print something out or access a
database without getting a PhD.

This led to OCaml, which seemed to have most of what I
wanted. Functional, but not obsessively so (you can printf when you
want to). Good execution speed. Support for objects. I read a lot of
literature about functional programming vs. object-oriented
programming and came to the conclusion that both have their uses so I
wanted a language that had both. I started writing some simple OCaml
programs as I was learning the language and I liked the way they came
out, no having to declare variable types, passing around functions and
the like. Then I got farther along in my studies, learning more about
how objects and classes are used in OCaml. I started looking at how
they handled the FP vs. OOP tension, namely adding functions to a
existing class/module vs. adding classes and subclasses, and they
started talking about parameterized classes and abstract modules and
the syntax started getting more and more complicated, and I started
thinking in the back of my mind "or, you could just use Lisp and have
multimethods".

So I went back and looked at the Lisp articles and such, and the
parentheses weren't looking so bad after all, especially when looking
at Lisp code in parentheses-aware editors. And we had multimethods,
and a simpler syntax for macros (OCaml has macros, but it's a whole
different syntax), etc, etc.

I would say that OCaml and Lisp give you much the same power to do
things, but my experience is that while doing the simple stuff may be
simpler in OCaml than in Lisp, doing the complicated stuff is simpler
in Lisp than in OCaml, and I planned on doing a lot more of the
complicated stuff than the simple stuff. Although people say Common
Lisp is a 'big' language, it's basically just parentheses and
keywords. I don't want to expend my brainpower wrestling with my
programming language, I want to expend it solving problems, and I
think Lisp is the best way to do this.

Especially since the problems I'm interested in are in the areas of
bioinformatics. The big Bio projects on the web are BioPerl, BioPython
and BioJava, but those languages don't offer the combination of speed
and power that OCaml and Lisp do, and in addition to Lisp's simplified
syntax my feeling is that there's more bioinformatics projects done in
Lisp than in OCaml, probably since it's been around longer and is more
well known.

## How far have you gotten in your study of Lisp? (I know, that is hard to measure)

Not too far, mainly reading the usual suspects (Ansi Common Lisp,
PAIP, some of On Lisp) plus writing some Common Lisp versions of
examples from "Beginning Perl for Bioinformatics."

## What do you think of Lisp so far?

When reading Lisp books and writng Lisp I feel like incredible power
is available at my fingertips. Functional, OO, imperative, symbolic
programming, code that writes code with macros, things you can
technically do with other languages, if you have enough time, but why
bother?
