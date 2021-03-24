````ruby
a = [1, 2, 3, 3]
b = a
c = a.uniq
````

On `line 1`, the local variable `a` is initialized to the array object `[1,2,3,3]`. On `line 2`, local variable `b` is initialized to the same array object that local variable `a` references/points to in memory. On `line 3`, the array object that local variable `a` references has the method `Array#uniq` called on it, which is a non mutating method that takes an array object and returns a new array that is the same as the array object it was called on, without any repeating elements. So when `Array#uniq` is called on the array object `[1,2,3,3]`, it returns the new array `[1,2,3]`. That new array object is used to initialize the local variable `c`. At this point, both variables `a` and `b` reference the same array object in memory, while local variable `c` references an entirely new one.

This code is a great example of how non mutating methods do not change the original object, yet return entirely new objects. When `Array#uniq` is called on the array that local variable `a` references, it does not change that array, but it does return a new object which is used to initialized local variable `c`. At the end, local variables `a` and `b` point to the same array object in memory, and its value is the same as it was on `line 2`.

(Just over 3 min)