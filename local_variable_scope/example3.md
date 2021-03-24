````ruby
a = 4
b = 2

loop do
  c = 3
  a = c
  break
end

puts a
puts b
````

The code displays `3` to the standard output and then returns `nil`. After that, it displays `2` to the standard output and then returns `nil`. On `line 1`, local variable `a` is initialized to the integer object `4`. On `line 2`, local variable `b` is initialized to the integer literal object `2`. On `line 4`, the `loop` method is invoked, and a `do..end` block is attached from `line4` to `line 8`. Inside the block, on `line 5`, local variable `c` is initialized to the integer object `3` within the scope of the block. On `line 6`, local variable `a`, which was initialized on `line 1` of the main method, is reassigned to the object that local variable `c` references, which is the integer object `3`. On `line 11`, the object that local variable `a` references (which is `3`) is used as an argument to the `puts` method, and so `3` is displayed to the standard output and then `nil` is returned. On `line 12`, the object that local variable `b` references (which is `2`) is used as an argument to the `puts` method, and so `2` is displayed to the standard output and `nil` is returned.

This code is another good example of how inner scope has access to local variables initialized in an outer scope (and thus how local variable `a` was reassigned inside the block on `line 6`, and then its value carried over when used as an argument to the `puts` method on `line 11`).



(<5 min)