```Ruby
animal = "dog"

loop do |animal|
  animal = "cat"
  break
end

puts animal
```
Line 8 will output `dog` and return `nil`.

On line 1, local variable `animal` is initialized and references a string object with the value `"dog"`.

On line 3, the `loop` method is invoked and passed a `do...end` block (lines 3 - 6) as an argument with one parameter, `animal`. Within the block, block local variable is assigned the string object `"cat"` and immediately breaks out of the loop.

On line 8, the `puts` method is invoked and passed `animal` as an argument, which will output its value. Because `puts` always returns `nil`, this is what gets returned.

This example demonstrates how **variable shadowing** can prevent variables to be used as intended. When the variable `animal` is assigned within the block, Ruby looks for the closest variable to use, starting inward and moving out. Because `animal` was assigned as a block parameter, this variable is found first, preventing `animal` on line 1 from ever being reassigned. For this reason, when passed as an argument on line 8, `animal`'s assignment to `"dog"` remains.