````ruby
arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

new_array = arr.select do |n| 
      n + 1
end
p new_array
````

On `line 1`, local variable `arr` is initialized to an array object `[1,2,3,4,5,6,7,8,9,10]`.

On `line 3`, the array object that local variable `arr` references has the `Array#select` method called on it, with a `do..end` block attached to the method from `line 3` to `line 5`.

`#select` first initializes a new array inside the method. Each time the block returns a truthy value, the current element at the index being iterated over will be added to the new array object.

During each iteration of the `#select` method, the element object at the current index of the array is yielded over to the attached block as an argument in order to initialize the block parameter `n`. 

On `line 4`, each time the block is ran, the object that block parameter `n` references is added to the integer object `1`, and that value is returned from the block to the `#select` method.

`#select` pays attention to the truthiness of the return value of the attached block. Since Ruby only considers `false` and `nil` to be falsy, and every other value to be truthy, every single value returned to `#select` will be a truthy value, and therefore every element from the array object that `#select` was called on will be placed inside the new array, and that will be returned.

This returned array object from the `#select` method called on `line 3` will be used to initialize the local variable `new_array` on `line 3`.

On `line 6`, the array object that `new_array` references (which is `[1,2,3,4,5,6,7,8,9,10]`) will be used as an argument to the `p` method, and so it will be displayed to the standard output and it will also be returned.

This code is a good example of how `#select` pays attention to the return value of the block, and does not actually transform elements based upon the code inside the block. Again, `#select` only cares about the return value and does not actually use the code inside the block to transform any elements.

(6 min)