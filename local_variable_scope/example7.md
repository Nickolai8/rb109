````ruby
a = 'Bob'

5.times do |x|
  a = 'Bill'
end

p a
````

This code will display `'Bill'` to the standard output, and then return `'Bill'`.

On `line 1`, the local variable `a` is initialized to a string literal object `'Bob'`. On `line 3`, the `Integer#times` method is called on the integer object `5`, so the `do..end` block will run 5 times. While this block has a block parameter `x`, it is never used.

On `line 4`, during each iteration of the block, local variable `a` is reassigned to a string literal object `'Bill'`. After 5 cycles of this, the `times` method is exited.

On `line 7`, the object that local variable `a` references (which is `Bill` at this point) is used as an argument to the `p` method, which displays the argument object to the standard output and then returns that same object.

This code is a great example of how a blocks inner scope has access to local variables initialized in an outer scope, in this instance local variable `a`. Note that the block parameter does not share the same variable name as `a`, so local variable `a` is not overshadowed.



(<3.5 min)