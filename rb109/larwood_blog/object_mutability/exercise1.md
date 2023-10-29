```Ruby def fix(value)
  value.upcase!
  value.concat('!')
  value
end

s = 'hello'
t = fix(s)
```
`s` and `t` will reference a string object with the value `'HELLO!'`.

On line 7, local variable `s` is initialized and references a string object with the value `'hello'`. On line 8, `s` is passed as an argument to the defined `fix` method, binding its value to the method's parameter `value`. Within the method, 2 destructive methods are called on `value`: `upcase!` changes all characters to uppercase and `concat('!')` concatenates `!` to the end of the string. The value of `value` is then returned from the method, assigning it to the initialized local variable `t`.

This example illustrates how Ruby appears to handle mutable objects as **pass-by-reference** when a destructive method is called on them. This behavior suggests that Ruby uses a *reference* to the original object, allowing the original object to be mutated. Because both methods within `fix` were destructive, the original object assigned to `s` on line 7 was mutated; therefore, its value matches that of `t`.