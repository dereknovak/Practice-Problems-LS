What is output on lines 9 and 10? Why?
```Ruby
def plus(x, y)
  x = x + y
end

a = 3
b = plus(a, 2)
puts a
puts b
```
The code will output `3` and `5` on separate lines.

On line 5, local variable `a` is initialized and references an integer object with the value `3`.

On line 6, `a` and the integer `2` are passed as arguments to the defined `plus` method invocation, binding the value of `a` to the method's parameter `x` and `2` to the other parameter, `y`. Within the method, `x` is reassigned to the sum of `x` and `y`, which evaluates to `5`. This value is returned from the method and gets assigned to the initialized local variable `b`.

On lines 7 and 8, both `a` and `b` are passed as arguments to the `puts` method invocation, which outputs their values to the console. Because `a` was never reassigned, just used for method invocation, its value remains as `3`.