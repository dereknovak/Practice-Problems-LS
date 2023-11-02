What is output? Why?
```Ruby
animal = 'dog'

case animal
when 'cat'
  puts 'Meow'
when 'dog'
  puts 'Woof'
else
  puts 'Silence...'
end
```
The code will output `Woof`.

On line 1, local variable `animal` is intialized and references a string object with the value `'dog'`. From lines 3-10, a `case` statement is employed, comparing each `when` branch to the value of `animal`. Because its value is `'dog'`, the `'dog'` branch is executed, which passes the string object `'Woof'` as an argument to the `puts` method invocation, outputting it to the console.