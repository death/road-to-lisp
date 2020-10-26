# John Pallister

## When did you first try Lisp (meaning here and throughout the survey "any member of the Lisp family") seriously, and which Lisp family member was it?

As part of the Knowledge Engineering course in the final year of my
undergrad Electrical Engineering degree (University of Canterbury [New
Zealand], 1991). We did assignments in Scheme (implementing a basic
backpropagation neural network, thereby killing two birds with one
stone), Prolog *etc*.

Thereafter I used C++ pretty much exclusively: writing distributed
simulations for my Master's, then application development (mainly for
Windows). I learned Java and then Python on the way, and the latter
re-introduced me to the power of `lambda`.

Skip forward to 2002...

As for which Lisp family member I'm using now, it's [Corman Common
Lisp](http://www.cormanlisp.com/). It's fast, cheap, ANSI compliant,
well-supported, comes with full source, and runs on the vast majority
of the world's computers; AFAIK, it's the only Lisp that meets all
those criteria. (Like I'd know.) The only thing wrong with it is that
it doesn't work with [ILISP](http://sourceforge.net/projects/ilisp/)
very well (or indeed at all, in my experience).

## What led you to try Lisp?

After leaving a lucrative contracting job in Amsterdam to come back to
Wellington, NZ and pursue my "masterpiece", it became apparent that
neither C++, Java nor Python were going to give me the combination of
"exploratory" development and good run-time performance I
needed. Since I was (and still am) learning everything as I went, I
needed a language that supported a very "flexible" development style,
and the prototypes I was building in Java were just too brittle.

Going in search of a better language, I soon found Paul Graham's
[site](http://www.paulgraham.com/), and his arguments convinced me
that Lisp really was The One True Way. It's the macros, of course. As
he explained in [On Lisp](http://www.paulgraham.com/onlisptext.html),
the ability to grow and extend the language quite so seamlessly in the
direction of the solution meant, for me, that *(a)* I didn't have to
design large pieces of the solution up-front so that it could be
implemented coherently, and *(b)* because the Lisp REPL could be a
part of the final system, that system could be massively more powerful
as a result.

My decision to go with Lisp has since been validated, I think, by the
way the whole code-is-data idea has permeated my entire design and
allowed me to imagine a system far more subtle, complex and yet
conceivably implementable than anything I could see myself writing in
C++, Java or any other language. And it still runs as fast, compiled
native code! *From the REPL!*

## If you were trying Lisp out of unhappiness with another language, what was that other language and what did you not like about it, or what were you hoping to find different in Lisp?

IMHO, C++ and Java are fine if one knows what one is trying to build
and how one going to build it. Particularly if you're writing a fairly
straightforward application to perform a well-understood task. If
however you're "feeling your way" towards a rather vague and nebulous
solution, you're going to spend an awful lot of time either
restructuring big chunks of code or rewriting stuff from scratch.

Python (and all the other, newer and "better" languages that I
*haven't* tried) is certainly an improvement, but if you're looking
for a better language, why not go with the best one you can find?

## How far have you gotten in your study of Lisp? (I know, that is hard to measure)

That is hard to say. I do like the way that, like C++, Lisp supports
multiple paradigms, so you can mix imperative, functional and OO
styles to suit the moment. This means that a lot of the concepts are
already familiar, and so I'm quickly writing useful software even
though I haven't mastered Lisp in any sense.

I've read through Graham's two books, and started
[SICP](http://mitpress.mit.edu/sicp/sicp.html) and Peter Norvig's
[PAIP](http://www.norvig.com/paip.html) (although I haven't opened
them lately - who has time?). I own Queinnec's [Lisp in Small
Pieces](http://youpou.lip6.fr/queinnec/WWW/LiSP.html), although I
don't think I'll be tackling that for a while.

I appreciated reading the [Tutorial on Good Lisp Programming
Style](http://www.norvig.com/luv-slides.ps) by Norvig and Pitman. I
need to persevere with the textbooks in order to be exposed to more
good style, but finding time is a challenge.

## What do you think of Lisp so far?

Believe the hype. Lisp kicks arse.

On the other hand, I agree with Paul Graham's idea that developing in
Lisp represents a competitive advantage, so I don't care whether the
rest of the programming world "sees the light" anytime soon. `;)`
