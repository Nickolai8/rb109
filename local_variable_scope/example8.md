````ruby
animal = "dog"

loop do |_|
  animal = "cat"
  var = "ball"
  break
end

puts animal
puts var
````

This code displays `'dog'` to the standard output, and then returns `nil`. After, an error is thrown and the program exits.

On `line 1`, the local variable `animal` is initialized to a string literal object `'dog'`. On `line 3`, the `loop` method is invoked with an attached `do..end` block spanning from `line 3` to `line 7`. Inside the loop, on `line 4`, local variable `animal` is reassigned to a string literal object `'cat'`. On `line 5`, local variable `var` is initialized to a string literal object `'ball'`. On `line 6`, a `break` is executed, and the loop is exited.

On `line 9`, the object that local variable `animal` references is used as an argument to the `puts` method, and so it is displayed to the standard output and then `nil` is returned. 

On `line 10`, the code attempts to use the object that local variable `var` references as an argument to the `puts` method, however this area does not have access to the local variable `var`, because `var` was initialized inside an inner scope, and thus an error is raised.

This code is a great example of how outer scope does not have access to variables initialized inside an inner scope(hence why `line 10` raised an error), but that inner scope does have access to local variables initialized inside an outer scope (hence why local variable `animal` was able to be reassigned on `line 4`)



< 4 min