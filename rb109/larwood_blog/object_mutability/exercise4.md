What value does `s` and `t` have? Why? What concept does this demonstrate?
```Ruby
def fix(value)
  value = value.upcase!
  value.concat('!')
end

s = 'hello'
t = fix(s)
```
In this code, both `s` and `t` will reference a string object with the value `'HELLO!'`.

On line 6, local variable `s` is initialized and references a string object with the value `'hello'`. On line 7, `s` is passed as an argument to the defined `fix` method invocation, binding its value to the method's parameter `value`. Within the method (lines 1 - 4), `value` is first reassigned to the returned value of calling the `upcase!` method on itself. Because `upcase!` is a destructive method, the object ID of `value` remains the same, only mutated to `'HELLO'`, making the reassignment redundant. Next, the `concat!` method is called on `value`, mutating its value by concatenating the string object `'!'` to the end. This value is returned from the method and assigned to the initialized local variable `t`. Because `s` and `value` remained bound throughout the entirity of `fix`, their value is identical.

This example illustrates how Ruby appears to handle mutable objects as **pass-by-reference** when a destructive method is called on them. This behavior suggests that Ruby uses a *reference* to the original object, allowing the original object to be mutated.