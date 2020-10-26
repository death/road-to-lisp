# Klaus Weidner

## When did you first try Lisp seriously, and which Lisp family member was it?

In 2003, using Common Lisp.

## What led you to try Lisp?

I've dabbled in Lisp a bit previously (some Emacs Lisp, and a couple
of experiments after reading Douglas Hofstadter's columns), but never
really saw the point of the language, programming in Lisp just seemed
weird. If I had heard some better arguments about it, I'd probably
have switched ten years ago.

As a short digression, here are some things which *didn't* lead me to
try lisp:

- the "recursive spirit that permeates lisp" (or however Hofstadter
  put it) - vaguely intriguing from a mathematician's point of view,
  but doesn't seem very relevant from a programmer's point of view. I
  was generating fractals in a Basic that didn't support recursion
  directly, and hadn't missed it very much.
- Emacs Lisp, or rather its documentation, just made programming in
  Lisp look extremely laborious and arcane. I was intrigued by GNU
  Calc and its power though, and that helped plant the meme that Lisp
  must be good at something.
- Guile being proposed as the "standard GNU extension language" in a
  rather clumsy way, with a lack of good arguments as to why, and no
  visible examples to show its power.
- The oft-repeated arguments about Lisp being a list-processing
  language (which sounds inefficient), an AI language (there's more to
  life than Eliza), and of course a slow interpreted language. I know
  now that these claims aren't true, but I hadn't seen them properly
  debunked until recently.

What got me more seriously interested was my continuing search for a
better language and environment - Perl got the job done but I had the
feeling that there had to be something better. I read about ML/ocaml,
haskell and related languages, prompted by the functional programming
contests and the "Great Programming Language Shootout".

The epiphany came when reading "On Lisp" by Paul Graham, that's when I
saw the light and realized that the weird parentheses and everything
else fit together perfectly and needed to be the way they are. I'd
agree that Lisp is one of the only two truly elegant programming
languages (Forth being the other one), and that it was more discovered
than developed.

## What other languages have you been using most?

I got started way back in the stone age (okay, cassette tape and 5.25"
floppy disk age) with Basic, then progressed (if that is the right
word) with C. I never really got into C++ despite spending a fair
amount of time with it - I read Scott Meyer's "Effective C++" books,
and was at the same time impressed by the trickery and disgusted by
the need for such trickery. The books planted the Lisp meme indirectly
by mentioning in passing how CLOS could do things that C++ had major
problems with.

I've been using Perl a lot, and while it's not a pretty language it
has been quite effective in getting the job done. But once
applications reached a certain size, it started creaking in the
corners, and (lack of) performance has also been an issue. Perl tempts
you to do everything using the available language constructs, even if
they aren't really appropriate for the problem. Things like using
regular expressions as an ad-hoc HTML "parser". Fixing it to do the
right thing would be orders of magnitude more work than the Perl way:
doing something that is is almost, but not quite, the solution to the
problem you needed solved.

## How far have you gotten in your study of Lisp?

Intrigued, and slowly starting to get the hang of things. I'm starting
to be able to program for minutes at a stretch now without having to
look something up in the HyperSpec :-)

## What do you think of Lisp so far?

Here's my shot at listing the things that make things beautiful and
unique:

- Macros, which allow you to introduce new control structures and
  totally change the way the language works (if that's what you need
  to do). Requires a non-syntactic language with direct access to the
  compiler's input.
- Being able to change the language to fit the application. Requires
  macros.
- A non-syntactic language that can be fully understood by an editor
  and tools. Requires the ugly parentheses :-)

Changing any of Lisp's surface features would almost certainly break
this.

Of course, CL is a huge language, and rather cluttered, and sometimes
the little things start to get seriously annoying (i.e. no atomic
rename, no portable way to read directory contents or stat(2) files,
etc.), where I am still spoiled by Perl/C's close match to the Unix
API I'm used to.

The "asdf" system is neat, but I groan each time I have to type
`(asdf:oos 'asdf:load-op :FOO)` - why oh why isn't this simply
`(asdf:load :FOO)` or something equally simple? Was that a deliberate
effort to keep things obscure and unfriendly?
