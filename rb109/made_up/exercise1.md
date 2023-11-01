What does the following code output? Why?
```Ruby
greeting = 'hello'

if greeting == 'hello'
  puts 'Say hello'
else
  puts 'Say goodbye'
end
```
The code will output `Say hello`.

On line 1, local variable `greeting` is initialized and references a string object with the value `'hello'`. From lines 3 - 7, an `if` statement is employed, which checks whether the value of `greeting` is equal to `'hello'`. Because this evaluates as true, the `if` branch is executed, which passes the string object `'Say hello'` as an argument to the `puts` method, outputting it to the console.