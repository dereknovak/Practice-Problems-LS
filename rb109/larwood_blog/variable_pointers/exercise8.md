What does the following code output? Why? What concept does this demonstrate?
```Ruby
def increment(x)
  x << `b`
end

y = 'a'
increment(y)
puts y
```

The code will output `ab`.

On line 5, local variable `y` is initialized and references a string object with the value `'a'`. On line 6, `a` is passed as an argument to the defined `increment` method invocation, binding its value to the method's parameter, `x`. Within the method, `b` is concatenated onto the value of `x` using `<<` operator, mutating the caller to reference the value `'ab'`.

On line 7, `y` is passed as an argument to the `puts` method invocation, which will output its value to the console.

This example demonstrates how Ruby appears to handle mutable objects as **pass-by-reference** when a destructive method is called on them, as it seems that a _reference_ to the original object is used and therefore the original object _can_ be mutated. In this case, the `<<` operator is a destructive method; therefore, the value referenced by `y` on line 5 was mutated.