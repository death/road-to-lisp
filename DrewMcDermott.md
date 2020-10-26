# Drew McDermott

## When did you first try Lisp seriously, and which Lisp family member was it?

In 1965 or 1966 I encountered Lisp 1.5 and became quite taken with
it. However, I couldn't actually run a Lisp program until I got to MIT
and got access to a PDP-n running some long-forgotten Lisp dialect. (I
don't think it even had a compiler.)

## What led you to try Lisp?

I was interested in AI. I started with IPL-V, Newell and Simon's
language. It looked like assembly language. Lisp seemed very odd by
comparison, but I soon realized just how elegant it was.

## Where did your road originate?

In the 1950s list processing seemed like a radical innovation in an
array-oriented world. IPL-V's basic datatype was the list, but in a
basically different form from Lisp. E.g., every list had a header cell
that pointed to the list's property list. Hence there was no unique
empty list; you could have as many empty lists as you wanted. There
was also no problem adding an element to a list. No need to write
`(setf (cadr l) (cons x(cadr l)))`; you just found the second element
of l and added element 'x' to it. If the list was empty, it became
non-empty. As I said, IPL-V looked like assembly language, but the
instructions were in a list. How meta is that? Anyway, I think it's
fair to claim that Lisp's property lists descended from those of
IPL-V. That would explain, for instance, why property lists aren't in
a-list format, which is otherwise very puzzling.

## How far have you gotten in your study of Lisp?

I have learned everything there is to know, and have now commenced
forgetting things.

## What do you think of Lisp so far?

I'm still withholding judgment :). Alternative answer: Lisp isn't
perfect, but you can fix almost all the problems! Wow!
