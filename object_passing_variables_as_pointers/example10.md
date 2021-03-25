````ruby
def cap(str)
  str.capitalize!   # does this affect the object outside the method?
end

name = "jim"
cap(name)
puts name 
````

This method displays `'JIM'` to the standard output and then returns `nil`.

On `line 5`, the local variable `name` is assigned to a string literal object `'jim'`. On `line 6`, the object that local variable `name` references is used as an argument to the `cap` method invocation (in which the `cap` method is defined on `line1` to `line 3`). The method definition uses the object used as an argument in the method invocation to initialize the method parameter `str`. The method parameter `str` and the local variable `name` initialized in the main method both reference the exact same object at this point.

On `line 2`, inside the `cap` method, the object that method parameter `str` references has the `String#capitalize!` method called on it, which is a method that changes the actual string object it is called on by making every letter a capital version. At this point, method parameter `str` and local variable `name` initialized in the main method still reference the same object, which is now `'JIM'`.

On `line 7`, the object that local variable `name ` references is used as an argument to the `puts` method, so `'JIM'` is displayed to the standard output and `nil` is returned.

This code is a good example of how using an object in a method invocation as an argument can cause permanent changes to the object itself.

(< 4 min)

























































````ruby
greeting = 'Hello'

loop do
  greeting = 'Hi'
  break
end

puts greeting
````

This code displays `'Hi'` to the standard output and then returns `nil`.

On `line 1`, the local variable `greeting` is initialized to a string literal object `'Hello'`. On `line 3`, the `loop` method is invoked with a `do..end` block attached spanning from `line 3` to `line 6`. Inside the block on `line 4`, local variable `greeting` is reassigned to a string literal object `'Hi'`. On `line 8`, the object that local variable `greeting` references is used as an argument to the `puts` method, and so it is displayed to the standard output and `nil` is returned. This code is a great example of how inner scope has access to local variables initialized in an outer scope, thus how local variable `greeting` was able to be reassigned on `line 4`.

2 min flat





















