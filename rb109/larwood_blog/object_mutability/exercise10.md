What does the following code output? Why?
```Ruby def add_name(arr, name)
  arr = arr + [name]
end

names = ['bob', 'kim']
add_name(names, 'jim')
puts names
```
The code will output `bob` and `kim` on separate lines.

On line 5, local variable `names` is initialized and references an array of strings, containing the elements `['bob', 'kim']`. On line 6, `names` and the string object `'jim'` are passed as arguments to the defined `add_name` method invocation. `add_name` contains 2 parameters, `arr` and `name`, with `names` being bound to `arr` and `'jim'` being bound to `name`. Within the method, `arr` gets reassigned to the returned value of concatenating `[name]` to the end of the `arr` array. This is possible because `name` gets assigned to an array object before concatenation by using square brackets. With that said, `+` is a non-mutating method; therefore, while the returned value from the method includes all 3 strings within the `arr` array, the original object is not mutated. This is why, when passed as an argument to the `puts` method on line 7, only the original 2 string objects assigned on line 5 are output.