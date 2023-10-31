What does the following code output?
```Ruby
num = 3
num = 2 * num
p num
```
The code will output `6`.

On line 1, local variable `num` is initialized and references an integer object with the value `3`. On line 2, `num` is reassigned to the product of `2` and `num`, which returns `6`. On line 3, `num` is then passed as an argument to the `p` method invocation, which outputs its value to the console.