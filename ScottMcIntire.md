# Scott McIntire

## When did you first try Lisp (meaning here and throughout the survey "any member of the Lisp family") seriously, and which Lisp family member was it?

I became quite interested in Lisp around 96 when Graham's book came
out.  A few years before that I had discovered Scheme and thought it
was the most beautiful language in the world. Since it was related, I
looked at Common Lisp but it looked ugly by comparison. It took more
experience developing software before I realized the error of my
ways. I don't think I used a Lisp system until 2000 which was
MCL. Since then I have used LispWorks and Allegro.

## What led you to try Lisp?

Two things:

- I wanted a language that I could use to investigate ideas and
  algorithms that wouldn't get in the way.
- I had been developing commercial software using the hybrid approach
  of an interpreted interactive language with an interface to C for
  speed.  From this experience, I wanted a language that could be as
  interactive as a scripting language, but generate compiled code when
  I was done. I came across Paul Graham's books and realized that this
  Holy Grail had been realized, it was called Common Lisp. Graham's
  discussion of how software development is really more experimental
  than people want to admit really struck a chord.  I was also
  dissatisfied with the state of the single dispatch object
  systems. This is also fixed by Common Lisp.

Along the way I've looked at most of the popular languages as well as
functional languages like SML, OCaml, and Haskell. As Graham mentions,
static typing is great if you're translating a spec into code. That's
not what happens in practice when developing software.

## If you were trying Lisp out of unhappiness with another language, what was that other language and what did you not like about it, or what were you hoping to find different in Lisp?

I was unhappy with scripting languages as they lacked speed and expressive power.

I was unhappy with languages like C++ that are, basically, a nightmare.

In the case of C++ things like:

- Memory management - can we say "what century is this?."
- Memory fragmentation - can we say 24x7 - not!
- The problems with the classic diamond object diagram.  Yeah, let me
  see, which order are the constructors called when I have a virtual
  base class...
- No reasonable mixins.
- Oh silly me, I forgot to declare my destructor virtual.

As far as other OO languages like Java, I find that the focus on a
single dispatch OO as the be-all end-all is quite annoying.  Design
patterns were suppose to be the next level in working with objects;
but, it seems clear that they are mainly used to fix up the problems
with method ownership and single dispatch.

Of course, one can always argue C++ is getting better and java is
improving.  C++ now has the STL, Java always has something new.  To
me, this is similar to the way XML has developed.  What you end up
with is "We'll just add layer N of this new framajama technology to
fix the problems in layer N-1, then everything will be fine."

## How far have you gotten in your study of Lisp? (I know, that is hard to measure)

I have been writing Lisp programs for my self on and off (more on than
off lately) for about 3 years. I think I am getting a better sense of
what I can do. I've written a number of utilities and done a few
medium size projects.

## What do you think of Lisp so far?

It gets better every day. It's interesting how you change your
approach to problems with Lisp. For instance, a few years back I wrote
some code in C++ to work with Fuzzy logic systems. After a month of
coding in my spare nights and weekends I had code that read in a spec
for a fuzzy system which could "fire" fuzzy rules. This amounted to
building a parse tree and walking over it to evaluate the rules.

Level I Lisp:

While learning Common Lisp, I wrote the same thing over a weekend. I
didn't have to write a parser for a spec, I used the Lisp reader -
DONE. I then walked over a rule tree to "fire" the fuzzy rules.

Level II Lisp:

I later realized that I could define a new macro that had the form of
the spec and let it create all the data objects in the background. I
could use the macro to also carefully check the arguments to the spec
as well as any constraints that a collection of arguments might need
to satisfy.  I could also call the compiler and get RULES THAT WERE
COMPILED - ding!

Is an interpreter written in C++ (or C for that matter) as fast as
compiled Common Lisp code? This example has given me a new perspective
about performance comparisons.
