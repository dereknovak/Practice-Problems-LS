```Ruby
a = "hi there"
b = a
a = "not here"

puts b
```
The code will output `hi there`.

On line 1, local variable `a` is initialized and references a string object with the value `"hi there"`. On line 2, local variable `b` is initialized and references the same string object as `a`. On line 3, `a` is reassigned to reference the string object `"not here"`.

On line 5, the `puts` method is invoked and passed `b` as an argument, which outputs its value to there console. Because the reassignment of `a` had no impact on the assignment of `b`, its value remained as `"hi there"`, which is what gets output.

This example demonstrates how Ruby employs its **variables as pointers** to an address space in memory, rather than containing object values within themselves.
