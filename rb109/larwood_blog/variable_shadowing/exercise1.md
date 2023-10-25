```Ruby animal = "dog"

loop do |_|  
  animal = "cat"  
  var = "ball"  
  break
end

puts animal
puts var
```
Line 9 will output `cat` and return `nil`. Line 10 will throw a `NameError` message.

On line 1, local variable `animal` is initialized and references a string object with the value `"dog"`. On line 3, the `loop` method is invoked and passed a `do...end` block (lines 3 - 7) as an argument. On line 4, `animal` is reassigned to `"cat"`. On line 5, block local variable `var` is initialized and references `"ball"`. The block is then immediately exited using the `break` command.

On line 9, the `puts` method is invoked, passing `animal` as an argument, which outputs its newly reassigned value. Because `puts` always returns `nil`, this is what gets returns. Line 10 attempts to perform the same operation on `var`; however, because `var` was never initialized outside of the block's scope, Ruby cannot locate the variable and therefore throws an error.

This example demonstrates how Ruby approaches _variable scope_ in regards to blocks. A block establishes its own scope that can access local variables initialized outside of it, but not the other way around.
