What is `a` and `b`? Why?
```Ruby
a = 5.2
b = 7.3
a = b
b += 1.1
```
`a` will reference a float object with the value `7.3`. `b` will reference a float object with the value `8.4`.

On line 1, local variable `a` is initialized and references a float object with the value `5.2`. On line 2, local variable `b` is initialized and references a float object with the value `7.3`. On line 3, `a` is reassigned to reference the same object as `b`. On line 4, `b` is then reassigned to reference the sum of itself and `1.1`, which is `8.4`. Because floats are immutable objects, the value change of `b` must be reassignment, which will have no impact on `a`.
