What is output on line 7? What is returned? Why? What concept does this demonstrate?
```Ruby
def a_method(string)
  string << ' world'
end

a = 'hello'
a_method(a)
p a
```
The code will output and return `'hello world'`.

On line 5, local variable `a` is initialized and references a string object with the value `'hello'`. On line 6, `a` is passed as an argument to the defined `a_method` method invocation, binding its value to the method's parameter `string`. Within the method, the string object `' world'` is destructively concatenated onto the `string`, mutating its value to `'hello world'`. Because `a` and `string` reference the same object, both variables' value is mutated.

On line 7, `a` is passed as an argument to the `p` method invocation, which both outputs and returns its value, unchanged. This is why the value's output is seen with quotation marks.

This example illustrates how Ruby appears to handle mutable objects as **pass-by-reference** when a destructive method is called on them. This behavior suggests that Ruby uses a *reference* to the original object, allowing the original object to be mutated. In this case, `<<` is a destructive method, therefore the original object is mutated.