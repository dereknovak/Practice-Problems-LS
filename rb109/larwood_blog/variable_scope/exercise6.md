```Ruby
arr = [1, 2, 3, 4]
counter = 0
sum = 0

loop do  
  sum += arr[counter]  
  counter += 1  
  break if counter == arr.size
end 

puts "Your total is #{sum}"
```
Line 11 will output `Your total is 10` and return `nil`.

On line 1, local variable `arr` is initialized and references an array of integers. The array contains 4 elements that reference the values `1`, `2`, `3`, and `4`.

Lines 2 and 3 initialize local variables `counter` and `sum`, both of which reference the integer `0`.

On line 5, the `loop` method is invoked, passing in a `do...end` block (lines 6 - 8) as an argument. Within the loop of the block, `sum` is reassigned to the sum of itself and the current element, and `counter` is reassigned to 1 more than itself. This allows `counter` to keep track of loop iterations that will `break` once the value of `counter` is equal to the size of `arr`. Its size is determined by calling the `size` method on `arr`, which returns `4`.

After 4 iterations of `loop`, `sum` will have been reassigned to the sum of all of the elements in `arr`, which is `10`. This value is interpolated into the string object `"Your total is #{sum}"`, which is passed as an argument to the `puts` method and outputs its value. Because `puts` always returns `nil`, this is what will be returned.

This example demonstrates Ruby's ability to use **string interpolation** to cleanly output a referenced object within a premade string object. It also demonstrates **variable scope** in regards to blocks. Because `sum` was going to be utilized outside of the block's scope for string interpolation, it needed to be initialized in the outer-scope; otherwise, a `NameError` message would have been thrown, due to Ruby not being able to find the local variable.