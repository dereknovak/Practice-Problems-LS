```Ruby def test(str)
  str += '!'
  str.downcase!
end

test_str = 'Written Assessment'
test(test_str)
puts test_str
```
The code will output `Written Assessment`.

On line 6, local variable `test_str` is initialized and references a string object with the value `'Written Assessment'`. On line 7, `test_str` is passed as an argument to the defined `test` method invocation, binding its value to the method's parameter: `str`. Within the method (lines 1 - 4), `str` is reassigned to the value of itself concatenated with the string object `!`. Because of this reassignment, the alias relationship between `str` and `test_str` is immediately broken, and therefore any destructive method called on `str` will have no impact on `test_str`.

This example demonstrates how Ruby appears to handle mutable objects as **pass-by-value** when called by a non-destructive method, as it seems that a copy of the original object is used and therefore the original object cannot be mutated. In this scenario, reassignment is considered a non-destructive operation.