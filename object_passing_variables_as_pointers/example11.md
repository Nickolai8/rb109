````ruby
a = [1, 3]
b = [2]
arr = [a, b]
arr

a[1] = 5
arr
````

On `line 1`, local variable `a` is initialized to the array object `[1,3]`. On `line 2`, local variable `b` is initialized to the array object `[2]`. On `line 3`, the object thats local variable `a` and local variable `b` reference are used as elements to create a new array object that references them, `[[1,3],[2]]`, which is used to initialize local variable `arr`.

On `line 4`, the object that local variable `arr` references(`[[1,3][2]]`) is returned.

On `line 6`, the first element in the array object that local variable `a` references is reassigned to the integer object `5`. The array object that local variable `a` references has now gone from `[1,3]` to `[1,5]`. This is the same object and therefore the method is mutating.

On `line 7`, the object that local variable `arr` references (`[1,5],[2]`) is returned. 

This code is a good example of how when variables reference the same object, that when the object is mutated that the change will show up to both variables. When the second element of the array object that local variable `a` references is reassigned, that mutates the array object that `a` references/points to, which is also the same object that the first element of the array object that `arr` references/points to.

(5-6 min)