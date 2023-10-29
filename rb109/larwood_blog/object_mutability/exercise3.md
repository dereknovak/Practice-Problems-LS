What values do `s` and `t` have? Why?
```Ruby
def fix(value)
  value << 'xyz'
  value = value.upcase
  value.concat('!')
end

s = 'hello'
t = fix(s)
```
`s` will reference a string object with the value `'helloxyz'`. `t` will reference a string object with the value `'HELLOXYZ!'`.

On line 7, local variable `s` is initialized and references a string object with the value `'hello'`. On line 8, `s` is passed as an argument to the defined `fix` method invocation, binding its value to the method's parameter `value`. Within the method (lines 1 - 5), the string object `'xyz'` is destructively concatenated onto `value` using the `<<` operator. `value` is then reassigned to the return value of calling the `upcase` method on itself. Because of this reassignment, the alias relationship between `value` and `s` is broken; therefore, any further destructive methods called on `value` will have no impact on `s`. Lastly, the `concat` method is called on `value`, concatenating `'!'` onto `value`. This new value is returned from the method and assigned to the initialized local variable `t`.

Because line 2 invoked a destructive method *before* the reassignment, the original object assigned to `s` on line 7 is mutated to `'helloxyz'`. However, the rest of the changes did not impact `s`, which is why only `t` references the value `'HELLOXYZ!'`.