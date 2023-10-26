```Ruby
a = 'Bob'

5.times do |x|  
  a = 'Bill'
end

p a
```
Line 7 will output and return `"Bill"`.

On line 1, local variable `a` is initialized and references a string object with the value `'Bob'.

On line 3, the `times` method is called on the integer `5` with one parameter, `x`, and is passed a `do...end` block (lines 3 - 5) as an argument. Although `5.times` instructs the block to be iterated 5 times, each iteration only reassigns `a` to reference the string `'Bill'`. Therefore, on the last iteration, the loop is complete and the reference to `'Bill'` remains.

On line 7, the value of `a` is passed as an argument to the `p` method, which outputs and returns its value with string syntax.

This example demonstrates how Ruby approaches **variable scope** in regards to blocks. A block establishes its own scope that can access local variables initialized outside of it, but not the other way around. This is the reason that `a` on line 4 is able to reassign, rather than be initialized.