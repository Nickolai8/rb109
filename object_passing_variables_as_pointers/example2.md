````ruby
a = "hi there"
b = a
a << ", Bob"
````

On `line 1`, local variable `a` is initialized to a string literal object `"hi there"`. On `line 2`, local variable `b` is initialized to the same string literal object in memory that local variable `a` references, which is `"hi there"`. On `line 3`, the string object that local variable `a` references (and also local variable `b`) is mutated by concatenating the original string and adding the string `", Bob"` to it as well. At this point, both local variable `a` and local variable `b` point to the exact same string literal object in memory, which is `"hi there, Bob"`

This code is great example of how variables are just pointers to objects in memory. When both local variable `a` and local variable `b` point to the same string literal object, and the mutating method `String#<<` is called on variable `a`, that method permanently alters the object at the memory location that local variable `a` points to. Since local variable `b` also points to the same object in memory, that change is also reflected for local variable `b` as well.



(3 minutes)