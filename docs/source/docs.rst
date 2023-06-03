Documentation
===================================

**TASEL** is small enough that the docs fit on one page!

Stack operations
----

``dup``
----
``dup`` duplicates the top item of the stack.

(n1 -- n1 n1)

``drop``
----
``drop`` drops (removes) the top item of the stack

(n1 n2 -- n1)

``swap``
----
``swap`` swaps the first two items on the stack

(n1 n2 -- n2 n1)

``over``
----
``over`` takes the second element from the top of the stack and duplicates it to the top of the stack

(n1 n2 n3 -- n1 n2 n3 n2)

``rot``
----
``rot`` rotates the top three elements of the stack. The third element from the top of the stack gets moved to the top of the stack, pushing the other two elements down.

(n1 n2 n3 -- n3 n1 n2)

``cs``
----
``cs`` clears the contents of the stack.

(n1 n2 n3 -- )

I/O Operations
----

``outl``
----
``outl`` outputs the top of the stack with a newline at the end, consuming it.

``outf``
----
``outf`` outputs the top of the stack (flush-ly) and consumes it.

``chr``
----
If the top of the stack is an integer, ``chr`` prints the ASCII value of that integer, consuming it.

``getl``
----
``getl`` gets a line of input.

``getc``
----
``getc`` gets one character of input.

Goto/Labels
----

``label:<label name>``
----
Creates a label to jump to with goto

``goto:<label name>``
----
Jumps to the given label

Conditional statements
----

``=``
----
Checks if the top two items on the stack are equal, consuming them. If they are, it pushes ``true``. Otherwise, it pushes ``false``.

``!``
----
Checks if the top two items on the stack are not equal, consuming them. If they aren't, it pushes ``true``. Otherwise, it pushes ``false``.

``<``
----
Checks if the second from top item on the stack is lesser than the top, consuming both. If they are, it pushes ``true``. Otherwise, it pushes ``false``.

``>``
----
Checks if the second from top item on the stack is greater than the top, consuming both. If they are, it pushes ``true``. Otherwise, it pushes ``false``.

``if-true:<label-name>``
----
If the top is the stack is ``true``, then jump to the given label. Doesn't consume the top, so it's good to put ``drop`` after it if you don't neet the boolean there.

``if-false:<label-name>``
----
If the top of the stack is ``false``, then jump to the given label. Does not consume the top.

Subroutines
----

``sub:<sub name>``
----
Defines a subroutine with the given name. Everything until ``--`` is the body of the subroutine. Eg, ``sub:hello    "Hello, world!" outl    --``. Recursion is not supported, and labels/gotos inside and outside of the subroutine cannot interact.
