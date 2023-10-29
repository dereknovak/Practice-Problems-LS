What values do `s` and `t` have? Why?
```Ruby
def fix(value)
  value = value.upcase
  value.concat('!')
end

s = 'hello'
t = fix(s)
```
`s` will reference a string object with the value `'hello'`. `t` will reference a string object with the value `'HELLO!'`.

On line 6, local variable `s` is initialized and references a string object with the value `'hello'`. On line 7, `s` is passed as an argument to the defined `fix` method, binding its value to the method's parameter `value`. Within the method (lines 1 - 4), `value` is first reassigned to the return value of calling the `upcase` method on itself. Because of this reassignment, the alias relationship between `value` and `s` is immediately broken; therefore, any destructive methods invoked on `value` will have no impact on `s`. Next, the `concat` method is called on `value`, concatenating the string object `!` on its value. This new value is returned from the method, assigning it to the initialized local variable `t`.

Because of the reassignment on line 2, `s` continues to reference `'hello'` established on line 6, while `t` references the new string object `'HELLO!'`.