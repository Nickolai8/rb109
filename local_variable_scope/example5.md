````ruby
def greetings(str)
  puts str
  puts "Goodbye"
end

word = "Hello"

greetings(word)
````



This code displays `'Hello'` to the standard output, returns `nil`, then displays `'Goodbye'` to the standard output and returns `nil` again.

On `line 6`, the local variable `word` is initialized with a string literal object `'Hello'`. On `line 8`, the `greetings` method is invoked with the object that local variable `word` references (which is a string literal object `'Hello'`) as an argument. The argument is used to initialize the parameter `str` for the `greetings` method. The object is sent to the method definition.

On `line 1` to `line 4`, a method named `greetings` that takes one parameter `str` is defined. On `line 2` inside the method, the object that the `str` method parameter references is used as an argument for the `puts` method. Since the method was invoked with the string literal object `'Hello'` as an argument, and that object was used to initialize the method parameter `str`, `'Hello'` is used as an argument to `puts` on `line 2`. `'Hello'` is displayed to the standard output, and then `nil` is returned. On `line 3`, a string literal object `'Goodbye'` is used as an argument to the `puts` method, and so `'Goodbye'` is displayed to the standard output, and then `nil` is returned.

This code is a good example of object passing in ruby. First the local variable `word` is initialized to a string literal object, then `word` is used as an argument to the `greetings` method, which is the same thing as just using the object that `word` references as an argument. This argument in the method invocation is used to initialize the parameter in the method definition. The method `greetins`  may not have access to the local variable `word`, but it does have access to the object that local variable `word` references and uses that object inside the method.



(8 min, garbage answer too. This time I focused way more on speed instead of accuracy. I need to learn for the test not try and fake my way to it. A better answer below: )









````ruby
def greetings(str)
  puts str
  puts "Goodbye"
end

word = "Hello"

greetings(word)
````

This displays `'Hello'` to the standard output, then returns `nil`, and then displays `'Goodbye'` to the standard output, and then returns `nil` again.

On `line 6`, the local variable `word` is initialized to a string literal object `'Hello'`. On `line 8`, the `greetings` method is invoked with the object that local variable `word` references used as an argument to the method invocation. The method invocation sends the string literal object to the method definition (which is on `line1` to `line 4`), and the method definition uses this object to initialize the method parameter `str`. 

Inside the method definition, on `line 2`, the object that method parameter `str` references (which is `'Hello'` for this invocation) is used as an argument to the `puts` method, which displays `'Hello'` to the standard output and then returns `nil`. On `line 3` , a string literal object `'Goodbye'` is used as an argument to the `puts` method, and so `'Goodbye'` is displayed on the standard output and `nil` is returned.

This code is a good example of how while methods do not have access to local variables initialized outside of the method definition, they can access objects referenced by local variables scoped to the main method when they are used as arguments in the method invocation.



(6 min or less, way better).

