What does `test(a)` return on line 6? What if we called `map!` instead of `map`?
```Ruby
def test(b)
  b.map { |letter| "I like the letter: #{letter}" }
end

a = ['a', 'b', 'c']
test(a)
```
Line 7 will return `["I like the letter: a", "I like the letter: b", "I like the letter c"]`

On line 5, local variable `a` is initialized and references an array of strings, containing the elements `['a', 'b', 'c']`.

On line 6, `a` is passed as an argument to the defined `test` method, binding its value to the method's parameter, `b`. Within the method (lines 1 - 3), the `map` method is called on `b` and passed a block as an argument with 1 parameter, `letter`. Upon each iteration of the block, an element of `b` is bound to `letter` and interpolated into the string object `"I like the letter: #{letter}"`,replacing its original value with the new value. This returns a transformed array from `map`, as well as from `test`.

If line 2 used the `map!` method instead, the return value would be the same. That being said, the original array object referenced by `a` would be mutated to include the string iterpolation, as `map!` is a destructive method. This contrasts the previous example, as `map` is non-destructive and therefore `a` would continue to reference the original object assigned on line 5.
