Explain why `Hello World!` is not output. What concept does this demonstrate? What could be changed within the code to output the string?
```Ruby
5 || puts('Hello World!')
```
This example demonstrates how conditional statements in Ruby will **short-circuit** once a condition is met, exiting the statement before all code can be executed. Within the code, the `||` logical operator is employed, which will execute the right operand only if the left operand is evaluated as false. Because all expressions in Ruby are evaluated as true, except `false` and `nil`, the integer `5` is considered truthy; therefore, the statement gets short-circuited and `puts('Hello World')` is never executed.

In order to execute the right operand, the first value would need to return either `'false'` or `'nil'`. This can be achieved with a comparison operator, such as `5 > 6` or a method that returns `nil`, such as `puts(5)`.