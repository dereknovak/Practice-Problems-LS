```Ruby
a = 4
b = 2

loop do  
  c = 3  
  a = c  
  break
end

puts a
puts b
```

Line 10 will output `3` and return `nil`. Line 11 will output `2` and return `nil`.

On line 1, local variable `a` is initialized and references an integer object with the value `4`. On line 2, local variable `b` is initialized and references an integer object with the value `2`.

On line 4, the `loop` method is invoked and is passed a `do...end` block (lines 4 - 8) as an argument. Within the block, local variable `c` is initialized and references the integer object with the value `3`. `a` is then *reassigned* to reference the same value as `c`. On line 7, a `break` is employed, which exits the loop immediately.

On lines 10 and 11, both `a` and `b` are passed as arguments to the `puts` method, which outputs their values to the console and returns `nil`, since the `puts` method always returns `nil`.

This example demonstrates how Ruby employs its **variables as pointers** to an address space in memory, rather than containing object values within themselves. Although `c` was initialized inside of the block's scope, when `a` was reassigned to reference its value, this simply instructed the variable to *point* to the same location as `c`. When passed as an argument on line 10, `c` was not considered a factor in the `puts` method invocation, and therefore an error was not thrown.