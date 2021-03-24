````RUBY
a = 4
b = 2

2.times do |a|
  a = 5
  puts a
end

puts a
puts b
````

This code will display `5` to the standard output, return `nil`, and then display `5` to the standard output again and return `nil` a second time. Then, the code will display `4` and return `nil`, and then display `2` and return `nil` for a fourth time.

On `line 1`, the local variable `a` is initialized to the integer object `4`. On `line 2`, local variable `b` is initialized to the integer object `2`. On `line 4`, the `Integer#times` method is called on the object `2`, which means that the attached `do..end` block will iterate twice. In the attached block, there is a block parameter `a`, which shadows over the local variable `a` initialized in the main method. Therefore, on `line 5`, when the variable `a` is initialized to the integer object `5` inside the block, the variable `a` refers to the block parameter `a` and not the local variable initialized in the main method. On `line 6`, the object that block parameter `a` references(which is `5`) is used as an argument to the `puts` method, and so `5` is displayed to the standard output, and then `nil` is returned. This happens two times. 

On `line 9`, the object that local variable `a` references (which is `4`) is used as an argument to the `puts` method, and so `4` is displayed to the standard output and `nil` is returned. On `line 10`, the object that local variable `b` references (which is `2`) is used as an argument to the `puts` method, and so `2` is displayed to the standard output and `nil` is returned.

This code is a good example of variable shadowing. While `line 5` may look like local variable `a` is being reassigned, the block parameter `a` actually overshadows the local variable, and thus inside the block all references to `a` can never be to the local variable initialized in the main method.



(<6 min, okay)