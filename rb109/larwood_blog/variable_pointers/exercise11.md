What is assigned to `arr` on line 5? Why?
```Ruby
a = [1, 3]
b = [2]
arr = [a, b]
arr[1] = 5
arr
```
On line 5, `arr` will reference an array object containing the elements `[[1, 3], 5]`.

On lines 1 and 2, local variables `a` and `b` are initialized and reference array objects containing the elements `[1, 3]` and `[2]`, respectively. On line 3, local variable `arr` is initialized and references an array object containing the values of `a` and `b`. This creates a 2-element nested array, `[[1, 3], [2]]`, as both `a` and `b` are array objects.

On line 4, the second element of `arr` is reassigned to the integer `5`. Because array indexing begins at 0, `arr[1]` represents the second element. The `[]=` method is destructive, therefore the original object referenced by `arr` is mutated.