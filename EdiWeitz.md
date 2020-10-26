# Edi Weitz

## When did you first try Lisp (meaning here and throughout the survey "any member of the Lisp family") seriously, and which Lisp family member was it?

I first worked with Lisp (or rather had to work with Lisp) during my
studies (math and CS) at the University of Hannover, Germany
in 1986. It wasn't Common Lisp - must have been some MacLisp variant,
the university had a couple of PDP machines at that time. (Data point:
I bought the Lisp book that my professor Dieter Müller wrote - ISBN
3-411-00628-5 - at that time. I couldn't find it anymore but a former
fellow student of mine was so nice to give me his copy.) I seem to
recall that I was pretty impressed by some of Lisp's features but
didn't pursue it any further because it wasn't available for my
personal computers (Apple II and Atari ST) and we had only very
limited access to the university's machines. I forgot about the
language (and most other CS stuff) when I started doing serious
math...

My second contact with Lisp was around 1996 when I gradually
moved away from Macs towards Linux. I started using Emacs and learning
Emacs Lisp and was, again, quite impressed by the language. However, I
only used Emacs Lisp for Emacs (obviously) and continued to do
"serious" work with Perl, C, and friends.

I finally moved to Common Lisp somewhere around 2000. I think I tried
[CMUCL](http://www.cons.org/cmucl/) on Linux and
[LispWorks](https://web.archive.org/web/20121127212826/http://wiki.alu.org/www.lispworks.com/)
on Windows first.

## What led you to try Lisp?

I think I'm mostly influenced by good books. I began to like Perl (OK,
now you can shoot me...) after reading the [Camel
book](http://www.oreilly.com/catalog/pperl2/) which I still like very
much. The first book that opened my eyes for Lisp was (surprise,
surprise) the [Giraffe book](http://www.oreilly.com/catalog/gnuext/) -
a wonderful book IMHO. And let me add that I find it quite ironic that
an O'Reilly book paved the way for Lisp given the fact that O'Reilly
is actively ignoring Lisp.

Later I came across a local book sale where they offered the German
translation of Graham's ["Ansi Common
Lisp"](http://www.paulgraham.com/acl.html) for 5 DM (around US$ 2 at
that time) and I bought it. Although the translation is rather bad I
liked the book (and what I read about Lisp) so much that shortly
thereafter I also ordered ["On
Lisp"](http://www.paulgraham.com/onlisp.html) and was lucky enough to
get a copy. These books (and Norvig's great
[PAIP](http://www.norvig.com/paip.html)) finally got me hooked.

What made Lisp stand out for me was its beauty and clarity compared to
the other languages I knew, probably because I'm a mathematician.

I also have to add that I began to read c.l.l in 2000 and that this
newsgroup has certainly assured me in keeping on track. I'm still
impressed by the wealth of interesting posts I can find there every
day and I'm grateful to people like Barry Margolin, Tim Bradshaw, Joe
Marshall, Duane Rettig, Steven Haflich, Erik Naggum, Kent Pitman, and
many others for sharing their knowledge with us mere mortals. But if
I'd have to pick one person which I think is the best Lisp promoter
around I'd certainly vote for [Paul
Graham](http://www.paulgraham.com/).

 If you were trying Lisp out of unhappiness with another language,
 what was that other language and what did you not like about it, or
 what were you hoping to find different in Lisp?

This one doesn't apply because I didn't try Lisp out of unhappiness
with other languages. But since I began to seriously work with CL I've
come to the conclusion that all other languages I know pale in
comparison.

## How far have you gotten in your study of Lisp? (I know, that is hard to measure)

I still have a **lot** to learn but I'm quite comfortable with CL
now - to a degree where I often "think" in Lisp although I have to
write something in Perl or PHP. I wrote five medium-sized libraries
([CL-PPCRE](http://weitz.de/cl-ppcre/),
[HTML-TEMPLATE](http://weitz.de/html-template/),
[CL-WHO](http://weitz.de/cl-who/), [CL-GD](http://weitz.de/cl-gd/),
and [CL-INTERPOL](http://weitz.de/cl-interpol/)) and a stand-alone GUI
application ([The Regex Coach](http://weitz.de/regex-coach/)) in Lisp
and I managed to sneak it into some of my commercial projects. These
include two Windows GUI apps, a full-blown dynamic website (using
[mod_lisp](http://www.cliki.net/mod_lisp) and
[UncommonSQL](http://www.cliki.net/uncommonsql)) for a soccer
sweepstakes, and a small testing framework. I also started the Common
Lisp [Cookbook](http://cl-cookbook.sf.net/) project in order to learn
more about the language.

## What do you think of Lisp so far?

It's wonderful, I love it. But that doesn't mean I don't think it can
be improved. Some remarks:

- I have a couple of wishes for the evolution of CL which mostly
  center around vendors agreeing on certain sub-standards for things
  that aren't part of ANSI CL, like multi-processing, sockets, FFI,
  data persistence, internationalization, Unicode, and so on. (The
  [ALU
  site](https://web.archive.org/web/20121127212826/http://alu.cliki.net/Standard)
  shows some efforts in this direction and there are also things like
  [UFFI](http://uffi.b9.com/) but I have yet to see the commercial
  vendors taking notice.)
- I have never worked with a [Lisp
  Machine](http://lemonodor.com/archives/000441.html) (follow this
  link and watch the videos if you haven't done already!!!) but from
  what I saw and read I'm convinced that the Lisp IDEs we now have
  could be much better. I don't want to resurrect the old Symbolics
  hardware and I don't want emulators, I just hope that the current
  state of affairs will evolve in this direction. (And, yes, I'm
  willing to pay for it.)
- \<heretical\>I don't think Common Lisp is the end of history. I hope
  that in a couple of years we'll have a new Lisp which will sport
  some significant additions (see first point) and at the same time
  get rid of some cruft. I'm keeping an eye on
  [Arc](http://www.paulgraham.com/arc.html).\</heretical\>
