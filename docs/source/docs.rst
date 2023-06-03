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

Output/input
----

