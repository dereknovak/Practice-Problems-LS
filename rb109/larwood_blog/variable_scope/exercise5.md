```Ruby
def greetings(str)
  puts str
  puts "Goodbye"
end

word = "Hello"
greetings(word)
```

The following code will output `Hello` and `Goodbye` on separate lines, and will return `nil`.

On line 6, local variable `word` is initialized and references a string object with the value `"Hello"`. On line 7, the defined `greetings` method is invoked. `word` is passed as an argument to `greetings` and is bound to its parameter, `str`.

Within the `greeting` method (lines 1 - 4), method local variable `str` and string object `"Goodbye"` are individually passed as arguments to the `puts` method, which outputs both values to the console. Because `puts` is invoked on the last line of the method, `nil` is returned, as `puts` always returns `nil`.

This example demonstrates a wide variety of functionality that Ruby offers, including method definition, invocation, as well as passing objects through source code with the use of **variables as pointers**. When the value of `word` was bound to method parameter `str`, both referenced, or *pointed to*, the same address space in memory, which held the string object `"Hello"`.