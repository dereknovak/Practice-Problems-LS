```Ruby
a = "hi there"
b = a
a << ", Bob"

puts a
puts b
```
Both lines 5 and 6 will output `hi there, Bob` and return `nil`.

On line 1, local variable `a` is initialized and references a string object with the value `"hi there'`. On line 2, local variable `b` is initialized and references the same string object as `a`. On line 3, the string object `", Bob"` is concatenated onto the value of `a`, mutating the original object. Because `a` and `b` reference the same object, both values are affected by the mutatation.

On lines 5 and 6, both `a` and `b` are passed as arguments to the `puts` method, which outputs their values. Because `puts` always returns `nil`, that is what gets returned from both methods.

This example demonstrates how Ruby employs its **variables as pointers** to an address space in memory, rather than containing object values within themselves.
