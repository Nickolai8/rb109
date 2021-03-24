````ruby
def fix(value)
  value.upcase!
  value.concat('!')
  value
end

s = 'hello'
t = fix(s)
````

This code does not return or display anything.

On `line 7`, the local variable `s` is initialized to a string literal object `'hello'`. On `line 8`, the `fix` method is invoked with the object that local variable `s` points to as an argument. The object that `s` references is used to initialize the `fix` method parameter `value`. The method parameter `value` and the local variable `s` scoped to the main method both point to the same object in memory right now.

On `line 2` inside the method, the object that the method parameter `value` references (`'hello'`)has the `String#upcase!` method called on it. This method is destructive as it takes the original string object it was called on and changes the object itself into a completely uppercased version.  On `line 3`, the object that method parameter `value` points to/references has the `String#concat` method called on it. This method is destructive, as it combines an additional string with the current string and changes the original object it was called on. At this point, local variable `s` scoped to the main method and method parameter `value` reference the same string literal object in memory, which is `'HELLO!'`. The last line of the method is just referencing the method parameter `value`, which returns the object it references to where the method was invoked. 

On `line 8`, that returned value ('HELLO!') from calling `fix(s)` is used to initialize the local variable `t`.

At this point, both local variables `s` and `t` point to/reference the same string literal object in memory.

This code is a good example of  how objects used as arguments in method invocations can be mutated from within a method definition even while the method definition does not have access to the local variable that was seemingly used as an argument inside the method invocation. The object that local variable `s` points to/references is actually altered from using it as an argument in invoking the `fix` method.



(8 min)