# Nonya B

## When did you first try Lisp seriously?

I started reading lisp books about two years ago. I've experimented
with lisp, although I've never done anything "serious".

## Which Lisp did you try?

CMUCL within emacs and ilisp.

## What let you to try Lisp?

I'm a long time emacs user. I have built some[1] emacs extensions and
enjoyed interacting with elisp. I found making incremental changes and
immediately testing them both enjoyable and productive.

Two books also motivated me to learn lisp. "The Pragmatic Programmer"
by Hunt and Thomas - a "mom and apple pie" book - recommends learning
a new language a year. I also picked up Graham's "OnLisp" and loved
it; apart from explaining why macros are so powerful, it's a good
read.

[1] (in my ~/emacs directory: cat *.el | grep def | wc returns 157)

## If you were trying Lisp out of unhappiness with another language, what was it and what did you not like about it, or what about Lisp were you hoping to find different?

I did not come to Lisp from unhappiness. I spend most of my day
programming C++. I *enjoy* working with C++. However, you asked what I
don't like about it. Here's some off the top of my head:

- No Multimethods. Stroustrup considered this. The syntax was
  something like: `void foo(virtual bar& b,virtual baz& bb)` or
  somesuch. It was rejected because it made the linker too complex. I
  did implement double-dispatch to implement the visitor
  pattern. However, it isn't nearly as nice as built in multimethods.
- I would like to see better macro support in C++. One idea would be
  to allow a user to manipulate a complier's parse tree (see OpenC++
  for an implementation.)
- Metaobject Protocol: Even very simple things like a `typeof`
  operator would be very useful. The typical argument for typeof goes
  something like `template<typename t1,typename t2> typeof(a+b)
  operator+(T1 a,T2 b);` Again, see OpenC++ for a metaobject protocol
  for C++.
- Let me overload the `.` operator. This makes the decorator pattern
  more practical. I believe this was once part of C with classes, but
  was removed because no one but Stroustrup was using it.
- I would love to have a mode that allowed me to interact with my
  code, make small changes, and immediately see how the change impacts
  my system. Of course, this is where Lisp's wins big.

## What other languages did you look at besides Lisp, and what did you think of them?

I am interpreting this question to mean "What languages have you
learned that you thought were interesting, but you didn't have an
immediate use for."

- J. This is an array-oriented language by Ken Iverson (of apl fame)
  and Roger Hui (programming wizard). J is great. The interaction
  language of my current project - an image processing spreadsheet -
  is called 'I' and it borrows heavily from J (although phrases are
  parsed left to right instead of J's right to left - and please don't
  write to tell me why right to left is superior; I do understand the
  arguments).
- Ruby. This is a nice clean language. The `yield` statement is well
  done. However, I already know both Perl and Python, and although I
  read the Ruby book by Thomas and Hunt I don't see it as worth
  switching.
- Python. Python's big win is it's ability to be embedded its
  interpreter.  The boost python library makes embedding python in C++
  trivial. In my opinion, embedding is python's big win.

## How far have you gotten in your study of Lisp?

I've ready several good books (I've actually read more about Lisp than
I've programmed).

- I've read Graham's OnLisp and Ansi Common Lisp cover to cover.
- I've read most of Kiczale's "The Art of the Metaobject Protocol"
- I've read most of Norvig's "Paradigms of Artificial Intelligence
  Programming"

## What do you think of Lisp so far?

- Macros are unbelievably powerful. As an example, in my image
  spreadsheet, I tell Lisp about what functions are available in the
  application through the socket. I then have lisp build macros that
  can be used to send messages to the spreadsheet. But wait, there's
  more!  Suppose I have the following code fragment:

```lisp
;; load an eroded image in cell 0 0
(setg (gref 0 0)
  (erode-image (load-image "/home/swd/micro_photos/DSCN4831.JPG"))
```

`setg` `gref` `erode-image` and `load-image` are all macros that build
message to be sent to the spreadsheet. However, the macros are built
such that the message isn't sent until the "root" of the expression is
reached. I'm not explaining this well, so let's look at some
code. Here's a function that builds my macros:

```lisp
(defun define-grid-bridge-function (grid-function stream)
  (let* ((name (grid-function-name grid-function))
	 (param-list-names
	  ;; first param is return, so ignore it
	  (rest (map 'list #'grid-function-parameter-name
				(grid-function-parameters grid-function)))))
    (eval
     `(defmacro ,(string-no-delims name)
	,(append
	  (mapcar #'string-no-delims param-list-names)
	  '(&optional; is-param))
	`(progn
	   (convert-op ,',stream ,',name)
	   ,,@(convert-params-for-bridge-function param-list-names
						  stream)
	   (format ,',stream ")")
	   (unless ,is-param (finish-command ,',stream)))))))
```

The interesting thing to look at is the is-param parameter. This is
false if the expression is at the 'root' - not a parameter to another
function. When this is not a parameter, the entire message is
sent. Something like that is impossible to do in any other language I
know[3].

- CLOS is amazing. Around methods, multimethods.

- Interacting with lisp is great.

Wish list:

Allow me to easily embed lisp in a C++ app. Let the C++ app drive.

[3] I just chased someone away from lisp with that code, didn't I?
Maybe I shouldn't include something so unreadable. Maybe it's hard to
read that function in Lisp, but the point is it can't even be done in
another language! And I'm a novice - there may be a more readable way
to express this function.
