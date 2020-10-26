# Gordon Weakliem

## When did you first try Lisp (meaning here and throughout the survey "any member of the Lisp family") seriously, and which Lisp family member was it?

April 2002, first with JScheme, then CLisp, currently more with Franz
Allegro

## What led you to try Lisp?

I heard Patrick Logan speak at a conference about building web
services with Scheme, which sounded interesting, so I read "The Little
Schemer".  Later, Paul Graham's writings, esp. "Beating the Averages",
but also because I was feeling the limitations of the Java / C# family
of languages.

# If you were trying Lisp out of unhappiness with another language, what was that other language and what did you not like about it, or what were you hoping to find different in Lisp?

As I get more experience as a programmer, I constantly find myself
trying to code in a more "meta" way.  C++ RTTI was a start, but pretty
crude.  Java has good reflection (though awkward via the reflection
API), but poor code generation capabilities.  C# has reflection and
code generation, but no built in parsing mechanism, and the APIs are
still clunky - the code you write looks nothing like what's generated.
Javascript actually has some pretty powerful constructs, but it's such
a crippled environment (browser, though Windows Script Host gives you
a bit more) that it's a non-starter.  I also liked the way The Little
Schemer develops algorithms by refactoring, but on a grander scale
than Java would allow (i.e. changing a function's behavior by changing
the signature to accept a function).  Finally, I liked the whole idea
of a REPL and being able to get immediate feedback on my work and not
having to wait for the compiler.

## How far have you gotten in your study of Lisp? (I know, that is hard to measure)

I've completed reading Graham's "ANSI Common Lisp".  I haven't done
anything useful with it.  I want to start reading "On Lisp" soon,
maybe I'll come up with a programming project so I can get some
practical experience with the language.

## What do you think of Lisp so far?

It's a great language, but I think that Lisp has some real problems
talking to the outside world.  In particular, I'm having a tough time
figuring out HTTP/HTML/XML support.  Allegro CL has support but it's
not especially well documented.  I haven't found anything dealing with
how to do FFI - I'm sure it's out there, but I haven't found it.
