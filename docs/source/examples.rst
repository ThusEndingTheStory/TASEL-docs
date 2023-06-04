Examples
===================================

Subroutines
----

.. code:: bash
  sub:greet
    -> name # Assign the top of the stack to name
    "Hello, &{name}!" outl # Output "Hello, " + the name variable + "!" (Note: interpolation only works with variables)
  --
  
  "world" call:greet # This prints Hello, world!
