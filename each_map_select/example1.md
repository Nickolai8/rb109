````ruby
array = [1, 2, 3, 4, 5]

array.select do |num|
   puts num if num.odd?
end
````

This code displays `1` to the standard output, then `3`, then `5`, and then it returns an empty array `[]`.

On `line 1`, local variable `array` is initialized with an array object `[1,2,3,4,5]`. On `line 3`, the `Array#select` method is called on the object that local variable `array` references (which is `[1,2,3,4,5]`. At the start of the `#select` method, a new collection is created/initialized inside the method. 

The `#select` method iterates over each element of the collection it was called on. For each iteration, the the `#select` method `yields` the current element being iterated over to the block to initialize the block parameter `num`. During each block iteration, the object that `num` references is displayed to the console if the number is odd. Each time the block is ran, it returns `nil` to the `#select` method. 

During iteration, the block will use the object that block parameter `num` references as an argument to the `puts` method if the object that `num` references is an odd number. So, when iterating over the collection `[1,2,3,4,5]`, elements `1`, `3`, and `5` are displayed to the console.

If the `#select` method receives a return value that is truthy from the block, it will place the current element being iterated over into the new collection. If not, it wont. In this code, each return value from the block is falsy because `puts` returns `nil`, and `nil` is one of two objects in ruby that has a falsy value. Since no truthy value is received, no element from the original collection is added to the new collection that was created inside the `#select` method. Once iteration is complete, `#select` returns the new collection, which is an empty array `[]`.

This code is a good example of how the `#select` method pays attention to the truthiness of the blocks return value, and how the `puts` method inside of a method's block can cause unintended consequences when used as the last line of code.



(10 min)