```Ruby
a = “Hello”
b = a
a = “Goodbye”

puts a
puts b
```

Line 5 will output `Goodbye` and return `nil`. Line 6 will output `Hello` and return `nil`.

On line 1, local variable `a` is initialized and references a string object with the value `"Hello"`. On line 2, local variable `b` is initialized and is set to reference the _same_ object as `a`. On line 3, `a` is then _reassigned_ to reference the string object `"Goodbye"`, which _does not_ change `b`'s assignment to `"Hello"`.

Both `a` and `b` are passed as arguments to the `puts` method, which outputs their values to the console. Because `puts` always returns `nil`, this is what we see from both expressions.

This example demonstrates how Ruby employs its *variables as pointers* to an address space in memory, rather than containing object values within themselves.