Why does `a` output a value, but `b` output an error? What can be changed to fix this bug?
```Ruby
a = 1
5.times do
  b = 2
end

loop do
  puts a
  puts b
end
```
This example illustrates how Ruby approaches **variable scope** in regards to blocks. A block establishes its own scope that can access local variables initialized outside of it, but not the other way around.

Local variable `a` is initialized outside of the `loop` method (line 6); therefore, Ruby was able to locate it when passed as an argument to the `puts` method invocation on line 7. On the contrary, local variable `b` was initialized within the block argument of the `times` method (line 2). Because the outer-scope of this block cannot access variables from within it, and blocks do not share scope amongst themselves, `b` cannot be found when passed as an argument to the `puts` method invocation and a `NameError` message is thrown.