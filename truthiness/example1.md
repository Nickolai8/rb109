````ruby
a = "Hello"

if a
  puts "Hello is truthy"
else
  puts "Hello is falsey"
end
````

This code displays `'Hello is truthy'` and then returns `nil`.

On `line 1`, local variable `a` is initialized to a string literal object `'Hello'`. On `line 3`, a conditional `if` statement triggers because since the object that is referenced by local variable `a` is neither `false` or `nil`, then that object has a `truthy` value and thus the expression `a` is evaluated as true, and the branch is ran. Inside the branch, `line 4`, a string literal object `'Hello is truthy'` is used as an argument to the `puts` method, which displays the object to the standard output and then returns `nil`. No other code belonging to that `if..else` statement is ran, because one branch (the first one) already did.

This code is a great example of how everything has a truthy value in Ruby except for `false` and `nil`. Since the object that local variable `a` references is not `false` or `nil`, then the conditional expression is evaluated to be true and the branch is executed.



(<4 min)