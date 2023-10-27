```Ruby
a = [1, 2, 3, 3]
b = a
c = a.uniq
```
`a` references `[1, 2, 3, 3]`
`b` references `[1, 2, 3, 3]`
`c` references `[1, 2, 3]`

On line 1, local variable `a` is initialized and references an array object containing the elements `[1, 2, 3, 3]`. On line 2, local variable `b` is initialized and references the same array object as `a`. On line 3, local variable `c` is initialized and references the returned value of calling the `uniq` method on `a`. This method removes any duplicate values after its first iteration, so `[1, 2, 3]` is returned. Because `uniq` is not a destructive method, the original object referenced by `a` is unchanged.

If line 3 was changed to `c = a.uniq!`, all 3 variables would reference `[1, 2, 3]`. This is because `uniq!` is a destructive method; therefore, when called on `a`, its value would be mutated. Because `b` is referencing the same object as `a`, it's value would also be affected by the mutation.