````ruby
def test(str)
  str  += '!'
  str.downcase!
end

test_str = 'Written Assessment'
test(test_str)

puts test_str
````

This code displays `'Written Assessment'` to the standard output and then returns `nil`.

On `line 6`, the local variable `test_str` is initialized to a string literal object `'Written Assessment'`. On `line 7`, the object that local variable `test_str` references (which is `'Written Assessment'`) is used as an argument to the `test` method invocation. The `test` method is defined on `lines 1-4`. 

Method `test` is defined with one parameter `str`.  When `test` is invoked, it uses the string literal object used as an argument( `'Written Assessment'`) to initialize the method parameter `str`.

Inside the method, on `line 2`, the method parameter `str` is reassigned to the value of the current object that it points to (which is `'Written Assessment'` with a string literal object `'!'` appended on the end of it. This is reassignment, and is therefore not mutating and therefore the method parameter `str` now points to a different object than when it was initialized. Method parameter `str` now no longer references the same object that local variable `test_str` (which was initialized in the main method) does.

On `line 3` inside the `test` method, the object that method parameter `str` currently references/points to has the `String#downcase!` method called on it. `String#downcase!` is a mutating method that alters the object by changing all of the alphabetical characters into lowercase characters. Since this is the last line of the method, this value (`'written assessment'`) is returned, although it is not used by the main method.

On `line 9`, the object that local variable `test_str` currently references (which is `'Written Assesment'`) is used as an argument to the `puts` method. `puts` then displays the object to the standard output and then returns `nil`.

This code is a good example of how while method variables inside a method definition can reference the same object that a local variable initialized in the main method does, that the method parameter/local variable scoped to the method being reassigned causes the parameter/local variable scoped to the method to point to a different object, and thus makes it impossible for it to mutate the object that was used as an argument in the method invocation.

(8.5 min)