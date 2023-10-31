What does the following code output? Why?
```Ruby
a = %w(a b c)
a[1] = '-'
p a
```
The code will output `["a", "-", "c"]`.

On line 1, local variable `a` is initialized and references an array of strings, containing the elements `(a b c)`. This specific syntax, along with a prepended `%w`, can be used when all array elements are string objects, allowing for easier user reading. On line 2, index 1 of `a`, indicated by `a[1]`, is reassigned to the string object `'-'`, mutating the original array. `a` is then passed as an argument to the `p` method invocation, which outputs its assigned value.