```Ruby
animal = "dog"

loop do |_|  
  animal = "cat"  
  var = "ball"  
  break
end

puts animal
puts var
```

Line 9 will output `cat` and return `nil`. Line `10` will throw a `NameError` message.

On line 1, local variable `animal` is initialized and references a string object with the value `"dog"`.

On line 3, the `loop` method is invoked, passing a `do...end` block (lines 3 - 7) as an argument. Within the block, `animal` is reassigned to reference the string `"cat"` and block local variable `var` is initialized to reference the string `"ball"`. The block is then immediately exited using the `break` command.

On line 9, `animal` is passed as an argument to the `puts` method, which outputs its value to the console. Because `puts` always returns `nil`, this is what is returned. On line 10, however, Ruby attempts to find `var` within the program's base scope, but because it was only initialized within the block, it cannot be located and therefore throws the error.

This example demonstrates how Ruby approaches **variable scope** in regards to blocks. A block establishes its own scope that can access local variables initialized outside of it, but not the other way around.