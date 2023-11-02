What is output? Why?
```Ruby
a = "Hello"

if a
  puts "Hello is truthy"
else
  puts "Hello is falsy"
end
```
The code will output `Hello is truthy`.

On line 1, local variable `a` is initialized and references a string object with the value `"Hello"`. From lines 3-7, an `if` statement is employed, which checks whether the value of `a` evaluates as true. Because all expressions in Ruby evaluate as true, except `false` and `nil`, the `if` branch is executed, which passes the string object `"Hello is truthy"` as an argument to the `puts` method invocation, outputting it to the console.