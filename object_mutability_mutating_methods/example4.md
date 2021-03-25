````ruby
def fix(value)
  value = value.upcase!
  value.concat('!')
end

s = 'hello'
t = fix(s)
````

Local variable `s` has the value `'HELLO!'` and local variable `t` has the value `'HELLO!'.

On `line 6` the local variable `s` is assigned to a string literal object `'hello'`. On `line 7`, the method `fix`, (which is defined on `line 1` to `line 4` with one parameter `value`) is invoked with the object that local variable `s` references as an argument. Method parameter `value` references the same object that local variable `s` references.

On `line 2`, inside the `fix` method, the object that method parameter `value ` references has the `String#upcase!` method called on it, which is a method that changes the object it is called on by changing all characters to their uppercase version. That mutated object is returned and used to reassign the method parameter `value` (note that this would be the same thing as calling `value.upcase!` by itself without reassigning `value`).

On `line 3` inside the method, the object that method parameter `value` references has the `String#concat` method called on it, with a string literal object (`'!'`) as an argument, which mutates the object it was called on by adding the argument object to the end of it.

At this point, both local variable `s`, and method parameter `value` reference/point to the same object.

This is the last line in the method, so the object that `value` references is returned from the method definition to where the method was invoked, and that value is used to initialize local variable `t`.

This code is a good example of how passing objects into a method can mutate the argument object, as initially the object that local variable `s` references was `'hello'` and now it is `'HELLO!'`. Local variabls `s` and `t` both point to the same object, `'HELLO!'`.

(7 min)