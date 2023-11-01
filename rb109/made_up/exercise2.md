What is output? Why?
```Ruby animal = 'cat'

if animal == 'dog'
  puts 'Woof'
else
  puts 'Meow'
end
```
The code will output `Meow`.

On line 1, local variable `animal` is initialized and references a string object with the value `'cat'`. From lines 3 - 7, an `if` statement is employed, which checks whether the value of `animal` is equal to `'dog'`. Because this evaluates as false, the `else` branch is executed, which passes the string object `'Meow'` as an argument to the `puts` method invocation, outputting it to the console.