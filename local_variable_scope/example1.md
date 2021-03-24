````ruby
a = “Hello”
b = a
a = “Goodbye”
puts a
puts b

````

The code displays `'Goodbye'` to the standard output, then it returns `nil`. After that, it displays `'Hello'` to the standard output, then returns `nil`. On `line 1`, local variable `a` is initialized with a string literal object `'Hello'`. On line 2, local variable `b` is initialized using the object that local variable `a` points to/references. On `line 3`, local variable `a` is reassigned to a string literal object `'Goodbye'`. On `line 4`, the object that local variable `a` references (which is `'Goodbye'`) is used as an argument to the `puts` method, which displays the object to the standard output and then returns nil. On `line 5`, the object that local variable `'b' ` references (which is `'Hello'`) is used as am argument to the `puts` method, which displays the object to the standard output and then returns `nil`.

This code is a good example of how reassignment does not mutate the original object. While local variable `b` was assigned to the same object as local variable `a` on `line 2`, when `a` is reassigned it does not influence the object that it pointed to/referenced before reassignment.





(4 min)