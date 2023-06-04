Examples
===================================

Subroutines
----
.. code-block:: console
    
    sub:greet
      -> name # Assign the top of the stack to name
      "Hello, &{name}!" outl # Output "Hello, " + the name variable + "!" (Note: interpolation only works with variables)
    --

    "world" call:greet # This prints Hello, world!
    
Goto/labels
----
.. code-block:: console
    
    # Print 'Hello!' forever
    label:again # Create a new label called 'again'
    "Hello!" outl # Print 'Hello!'
    goto:again # Jump to the label 'again'

.. _
.. ----
.. .. code-block:: console
    
    _
