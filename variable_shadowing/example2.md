````ruby
n = 10

1.times do |n|
  n = 11
end

puts n
````

This code displays `10` to the standard output, and then returns `nil`.

On `line 1`, local variable `n` is initialized to the integer object `10`. On `line 3`, the `Integer#times` method is called on the integer object `1`, and therefore the attached `do..end` block is ran once. This attached `do..end` block has a block parameter `n`, which is the same name as the local variable `n` initialized in an outer scope.

On `line 4` inside the block, block parameter `n` is reassigned to the integer object `11`. 

On `line 7`, the object that local variable `n` references(which is `10`) is used as an argument to the `puts` method. `10` is then displayed to the standard output, and then `nil` is returned.

This code is a good example of variable shadowing. While it may appear as if local variable `n` is being reassigned inside the block on `line 4`, in reality the block has a parameter named `n`, and inside the block any calls to a variable in which both a local variable and a block parameter with the same name exists will refer to the block parameter and not the local variable.



(<4 min)