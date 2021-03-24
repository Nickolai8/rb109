````ruby
a = "hi there"
b = a
a = "not here"
````

On `line 1`, the local variable `a` is initialized to a string literal object `"hi there"`. On `line 2`, local variable `b` is initialized with the object referenced by local variable `a`, which is a string literal object `"hi there"`. Note that at this point, local variable `a` and local variable `b` both point to the same object in memory. On `line 3`, local variable `a` is reassigned to a string literal object `"not here"`. At this point, local variable `a` and local variable `b` point to different objects in memory.

This code is a great example of how variables are just pointers/references to objects in memory. While local variable `a` is being reassigned to a new object on `line 3`, assignment is not mutating the original object in memory where local variable `a` used to point, so local variable `b` is unaffected by the reassigning of local variable `a` and continues pointing at the object that local variable `a` previously pointed to.



(~ 3 min)

