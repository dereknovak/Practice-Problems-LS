```Ruby
a = 4

loop do  
  a = 5  
  b = 3

  break
end

puts a
puts b
```

Line 10 will output `5` and return `nil`. Line 11 will output a `NameError` message and will exit the program.

On line 1, local variable `a` is initialized and references an integer object with the value `4`.

On line 3, the `loop` method is invoked and is passed a `do...end` block (lines 3 - 8) as an argument. Within the block, `a` is *reassigned* to the integer `5`. Local variable `b` is then initialized and references the integer object `3`. Line 7 then employs a `break` to exit the loop immediately.

On lines 10 and 11, both `a` and `b` are passed as arguments to the `puts` method, which *should* output both values to the console and return `nil`, since the `puts` method always returns `nil`. Line 10 does so successfully, as `a` has been initialized outside of the previous block's scope; *however*, `b` was never initialized outside of the block's scope, causing Ruby to throw an error because it cannot locate the local variable.

This example demonstrates how Ruby approaches **variable scope** in regards to blocks. A block establishes its own scope that can access local variables initialized outside of it, but not the other way around. In this instance, `b` was initialized *inside* the block's scope, but never outside.