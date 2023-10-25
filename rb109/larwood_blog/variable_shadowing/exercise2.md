```Ruby
n = 101.times do |n|
        n = 11
    end

puts n
```
This code snippet will output `101` and return `nil`.

On line 1, the `times` method is called on an integer object with the value `101`. Within the same line, local variable `n` is initialized and references the returned value of the `times` method call. Because `times` always returns the calling object, `101` is returned and assigned the `n`.

On line 5, the `puts` method is invoked and passed `n` as an argument, which outputs its value to the console. Because `puts` always returns `nil`, this is what gets returned.

This example demonstrates how **variable shadowing** can make it difficult to understand how objects are being referenced in Ruby source code. On line 2, `n` is set as both a newly initialized variable as well as a parameter within the block. While the blocks operation ultimately did not influence what was returned and assigned to the `n` outside the block's scope, it's still a very confusing way to write the code.