What will be returned on line 3? Why? Can you identify an edge case involving an integer that would cause this code to fail?
```Ruby
number = 5

number > 6 ? "Greater than 6!" : "Less than 6..."
```
The ternary operator on line 3 will return `"Less than 6..."`.

On line 1, local variable `number` is initialized and references an integer object with the value `5`. On line 3, a ternary operator is employed, which checks wheter the value of `number` is greater than the integer `6`. Because this evaluates as false, the string object `"Less than 6..."` will be returned, as expressions to the right of the `:` are executed when the conditional statement is falsy.

One edge case that is overlooked is if `number` is assigned to the integer `6`. Because `6` is not greater than `6`, the falsy expression will be executed; however, this is deceptive because the values are equal.