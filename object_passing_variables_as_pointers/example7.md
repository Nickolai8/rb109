````ruby
def plus(x, y)
  x = x + y
end

a = 3
b = plus(a, 2)

puts a
puts b
````

This code displays `3` to the standard output, then returns `nil`. After, it displays `5` to the standard output then returns `nil`.



On `line 5`, the local variable `a` is initialized to the integer object `3`. On `line 6`, the `plus` method that has two parameters `x` and `y` was defined on `lines 1-3` is invoked with the object that local variable `a` references as the first argument, and the integer object `2` as the second argument. These arguments are sent to the method definition in order to initialize the method parameters, `x` and `y` respectively.

`plus` method parameter `x` is initialized to reference the integer object `3`, and method parameter `y` is initialized to reference the inter object `2`.

On `line 2` inside the `plus` method, the return values of method parameters `x` and `y` (which are `3` and `2` respectively) are added together, and method parameter `x` is reassigned to that int object (which is `5`). Since this is the last line in the method, that value is returned to where the method was invoked on `line 6`. The return value, which is `5` is used to initialize local variable `b`.

On `line 8`, the object that local variable `a` references (which is `3`) is used as an argument to the `puts` method, so `3` is displayed on the standard output, and `nil` is returned. On `line 9`, the object that local variable `b` references (which is `5`) is used as an argument to the `puts` method, so `5` is displayed to the standard output and `nil` is returned.

This is a good example of how objects can be passed as arguments of a method invocation to a method definition in order to initialize method parameters, and how methods can return values back to where they were invoked.

(7 min?)