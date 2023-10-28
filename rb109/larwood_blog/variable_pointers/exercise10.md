What does the following code output? Why? What concept does it demonstrate?
```Ruby
def cap(str)
  str.capitalize!
end

name = 'jim'
cap(name)
puts name
```
The code will output `Jim`.

On line 5, local variable `name` is initialized and references a string object with the value `'jim'`. On line 6, `name` is passed as an argument to the defined `cap` method invocation, binding its value to the method's parameter, `str`. Within the method, the destructive `capitalize!` method is called on `str`, mutating its value to `Jim`. Because `str` and `name` are aliases, both variables are affected by the object mutation.

On line 7, `name` is passed as an argument to the `puts` method invocation, outputting its value to the console.

This example demonstrates how Ruby appears to handle mutable objects as **pass-by-reference** when a destructive method is called on them, as it seems that a _reference_ to the original object is used and therefore the original object _can_ be mutated.