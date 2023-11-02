What is output? Why?
```Ruby
def test
  puts "written assessment"
end

var = test

if var
  puts "written assessment"
else
  puts "interview"
end
```
The code will output `written assessment` and `interview` on separate lines.

On line 5, the defined `test` method is invoked. Within the method (lines 1-3), the string object `"written assessment"` is passed as an argument to the `puts` method invocation, which outputs it to the console. Because this is the last line of the method, the method will return `nil` and assign it to the initialized local variable `var`.

From lines 7-11, an `if` statement is employed, which checks whether the value of `var` evaluates as true. `nil` is considered a falsy expression in Ruby; therefore, the `else` branch will be executed, which passes the string object `"interview"` as an argument to the `puts` method invocation, outputting it to the console.