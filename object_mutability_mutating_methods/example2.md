````ruby
def fix(value)
  value = value.upcase
  value.concat('!')
end

s = 'hello'
t = fix(s)
````

This method doesn't display or return anything. On `line 6`, local variable `s` is initialized to a string literal object `'hello'`. On `line 7`, the object that local variable `s` references is used as an argument for the `fix` method invocation. The `fix` method definition uses this argument object to initialize the method parameter `value` so that it references this object.

Method `fix` is defined on `lines 1-4`. On `line 2`, the object that `value` references has the `String#upcase` method called on it. This method is non mutating, and returns a new string that is an all upper case version. This return value is used to reassign `value` on `line 2`. Since the method parameter `value` was reassigned, it now points to a different object than the local variable `s` initialized in the main method.

On `line 3`, the object that parameter `value` references has the `String#concat` method called on it, in which it uses `'!'` as an argument. This method is mutating, and takes the original string object it was called on and destructively adds the argument to the end of it. This is the last expression in the method, so this is the value that is returned to where it is called, on `line 7`. The value returned is `'HELLO!'`, which is used to initialize local variable `t` in the main method on `line 7`.

Local variable `s` references a string literal object of `'hello'` and local variable `t` references a different string literal object, `'HELLO!'`.

This code is a good example of how when a method parameter is reassigned inside the method, that it loses the ability to mutate outside objects because the reference to the object that was passed as an argument to the method invocation is lost.

(9 minutes)