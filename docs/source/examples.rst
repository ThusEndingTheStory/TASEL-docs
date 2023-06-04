Examples
===================================

Just a couple of examples, because it's nice to have them! 👍

Subroutines
----
.. code-block:: julia
    
    sub:greet
      -> name # Assign the top of the stack to name
      "Hello, &{name}!" outl # Output "Hello, " + the name variable + "!" (Note: interpolation only works with variables)
    --

    "world" call:greet # This prints Hello, world!
    
Goto/labels
----
.. code-block:: julia
    
    # Print 'Hello!' forever
    label:again # Create a new label called 'again'
    "Hello!" outl # Print 'Hello!'
    goto:again # Jump to the label 'again'
    
Conditional/If
----
.. code-block:: julia
    
    "bar" -> foo
    foo "bar" = # In this case, it pushes true to the stack, because foo == "bar"
    if-true:trueCaseLabel # If the top is true, go to the label trueCaseLabel
    if-false:falseCaseLabel # The same, but if false and going to falseCaseLabel
    label:trueCaseLabel
        "Foo is bar!" outl
        goto:endFooBarCase
    label:falseCaseLabel
        "Foo is not bar!" outl
    label:endFooBarCase
    drop # Drops the true off of the stack, because if-true and if-false doesn't consume anything, and junk on the stack is bad

.. _
.. ----
.. .. code-block:: julia
    
    _
