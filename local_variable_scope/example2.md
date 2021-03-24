````ruby
a = 4

loop do
  a = 5
  b = 3


  break
end

puts a
puts b
````



This code displays `5` to the standard output, and then returns `nil`, and after that it displays an error message to the consol. On `line 1`, local variable `a` is initialized to the integer object `4`. On `line 3`, the `loop` method is invoked, with a `do..end` block attached from `line 3` to `line 9`. On `line 4`, the local variable `a` that was initialized in the main method on `line 1` is being reassigned to the integer object `5`. On `line 5`, the local variable `b` is initialized with the integer object `3`.  On `line 8`, the object that local variable `a` references (which is `5`) is used as an argument for the `puts` method, and `5` is displayed to the standard output and `nil` is returned. On `line 9`, the `puts` method is trying to use the object that local variable `b` references as an argument, but it does not have access to the local variable `b` and therefore an error is raised.

This code is a good example of local variable scope and how outer scope does not have access to variables that are initialized in an inner scope(which is why `puts` on `line 9` raised an exception), while the inner scope does have access to the variables of an outer scope (which is how local variable `a` was reassigned on `line 4`.)



(5 min)