````ruby
animal = "dog"

loop do |animal|
  animal = "cat"
  break
end

puts animal
````

This code displays 	`'dog'` to the standard output and then returns `nil`.

On `line 1`, the local variable `animal` is initialized to a string literal object `'dog'`.

On `line 3`, the `loop` method is invoked with an attached `do..end` block spanning from `line 3` to `line 6`. The block has a block parameter `animal`.

On `line 4`, the block parameter `animal` is initialized to a string literal object `cat`, where as many might assume that the local variable `animal` is being reassigned.

On `line 8`, the object that local variable `animal` references (which is `'dog'`) is used as an argument to the `puts` method, and so it is displayed to the standard output and `nil` is returned.



This code is a solid example of how when block parameters share the same name as local variables initialized in an outer scope, that the code inside the block references the block parameter instead of the local variable. The local variable `animal` was shadowed by the block parameter `animal`, and thus the code inside the block does not have access to it.



3-4 min