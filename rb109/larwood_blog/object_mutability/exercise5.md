What values to `s` and `t` have? Why? What concept does the example demonstrate?
```Ruby
def fix(value)
  value[1] = 'x'
  value
end

s = 'abc'
t = fix(s)
```
In this code, both `s` and `t` will reference a string object with the value `'axc'`.

On line 6, local variable `s` is initialized and references a string object with the value `'abc'`. On line 7, `s` is passed as an argument to the defined `fix` method invocation, binding its value to the method's parameter `value`. Within the method, the first index value is reassigned to the string object `'x'`, which mutates the original string object to `'axc'`. This value is return from the method and assigned to the initialized local variable `t`. Because `s` remained bound to `value` throughout the method, its value will be identical to that of `t`.

This example illustrates how Ruby appears to handle mutable objects as **pass-by-reference** when a destructive method is called on them. This behavior suggests that Ruby uses a *reference* to the original object, allowing the original object to be mutated. In this case, `[]=` is a destructive method, therefore the original object is mutated.