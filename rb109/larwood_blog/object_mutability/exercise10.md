What does the following code output? Why?
```Ruby
def add_name(arr, name)
  arr = arr << name
end

names = ['bob', 'kim']
add_name(names, 'jim')
puts names
```
The code will output `bob`, `kim`, and `jim` on separate lines.

On line 5, local variable `names` is initialized and references an array of strings, containing the elements `['bob', 'kim']`. On line 6, `names` and the string object `'jim'` are passed as arguments to the defined `add_name` method invocation. `add_name` has 2 parameters, `arr` and `name`, with `names` getting bound to `arr` and `'jim'` getting bound to `name`.

Within the method, `arr` is reassigned to the returned value of appending `name` onto itself. This creates a third element in the array, assigning its value to `'jim'`. Because `<<` is a destructive method, the original object reference by `names` and `arr` is mutated to `['bob', 'kim', 'jim']`.

On line 7, `names` is passed as an argument to the `puts` method invocation, which outputs each element of its array to a separate line in the console.