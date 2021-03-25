````ruby
arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

arr.select { |n| n.odd? }
````

This method returns an array object `[1,3,5,7,9]`. It does not display anything.

On `line 1`, local variable `arr` is initialized to an array object `[1,2,3,4,5,6,7,8,9,10]`.

On `line 3`, the array object that local variable `arr` references has the `Array#select` method called on it. First, `#select` initializes a new array object inside the method.`#select` then iterates over an array index by index, and yields the element object in the current index position over to the attached block as an argument, and the block uses this object to initialize the block parameter (in which this case it is `n`). During each iteration, the object that block parameter `n` references has the `Integer#odd?` method called on it, which returns either a `true` or `false` object depending on whether or not the integer object is odd or even respectively.

The `#select` method pays attention to the truthiness return value of the block. When the block returns a truthy value to the method, it places the current element being iterated over inside the new collection. In this case, only elements `1`, `3`, `5`, `7` and `9` make it into the new collection.

At the end of the `#select` method, the new collection object (`[1,3,5,7,9]`) is returned. 

This code is a good example of how select pays attention to the truthiness of the return value of the block.

(~5 min)