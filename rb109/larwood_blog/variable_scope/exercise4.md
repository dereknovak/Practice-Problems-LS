```Ruby
def example(str)
  i = 3
  loop do
    puts str
    i -= 1
    break if i == 0
  end
end

example('hello')
```

The following code will output `hello` 3 times, on separate lines and return `nil`.

On line 10, the defined method `example` method is invoked. The string object `'hello'` is passed in as an argument and is bound to the method's parameter, `str`.

Within the method (lines 1 - 8), method local variable `i` is initialized and references an integer object with the value `3`. On line 4, the `loop` method is invoked and passed a `do...end` block (lines 3 - 7) as an argument. Within the block, the `puts` method is invoked and is passed `str` as an argument, ouputting `hello` to the console. `i` is then *reassigned* to 1 less than itself, with the instruction to `break` from the loop once its value is equal to the integer `0`.

The block iteration is repeated 2 more times, as the value of `i` is reassigned to `1`, then to `0`, ouputting `hello` on each iteration. Once the condition is met, both the loop, then immediately the method are exited. Because the `loop` method always returns `nil`, and it is the last line of the method, the method itself will return `nil`.

This example demonstrates how Ruby utilizes a **call stack** to manage the order in which method and block invocation takes place, adding and removing operations from the top of the stack until the program concludes. The programs starts with the `example` method invocation on line 10, adding and removing each block iteration before moving onto the next, and finally returning back to line 10 *only* once all iterations have been completed.



