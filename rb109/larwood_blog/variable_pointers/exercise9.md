What does the following code output? Why? What concept does this demonstrate?
```Ruby
def change_name(name)
  name = 'bob'
end

name = 'jim'
change_name(name)
puts name
```
The code will output `jim`.

On line 5, local variable `name` is initialized and references a string object with the value `'jim'`. On line 6, `name` is passed as an argument to the defined `change_name` method invocation, binding its value to the method's parameter, `name`. Within the method, `name` is reassigned to the string object `'bob'`.

On line 7, `name` is passed as an argument to the `puts` method invocation, which outputs its value to the console.

This example demonstrates how Ruby appears to handle mutable objects as **pass-by-value** when a non-destructive method is called on them, as it seems that a _copy_ of the original object is used and therefore the original object _cannot_ be mutated. In this scenario, the reassignment is not considered a destructive operation; therefore, the value of `name` assigned on line 5 remains.