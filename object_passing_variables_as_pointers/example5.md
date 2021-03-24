````ruby
a = 5.2
b = 7.3

a = b

b += 1.1
````



On `line 1`, local variable `a` is initialized to the float object `5.2`. On `line 2`, local variable `b` is initialized to the float object `7.3`. On `line 4`, local variable `a` is reassigned to the object that local variable `b` references, which is the float object `7.3`. At this point, both local variables `a` and `b` point to the same object in memory, which is `7.3`. On `line 6`, local variable `b` is reassigned to the value of the current object it points to (`7.3`) and `1.1`, which is the float object `8.4`. At this point, local variables `a` and `b` point to different objects. Nothing is displayed or returned.

This code is a great example of how reassignment is not mutating. While local variable `b` might appear to be adding `1.1` to the object that it previously pointed to, it is actually being reassigned with the value returned by the expression `7.3 + 1.1`. 



(Just over 3 min)