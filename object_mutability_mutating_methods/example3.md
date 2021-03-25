````ruby
[1, 2, 3].all? do |num|
  num > 2
end
````

On `line 1`, the array object `[1,2,3]` has the `Array#all?` method called on it. `Array#all?` iterates over the array object by index, and for each iteration yields the element in the current index position over to the attached block as an argument so that the block can initialize its block parameter `num`. During each time the block is ran, it compares the object that block parameter `num` references with the integer object `2` to see if it is numerically greater than 2. If it is, the block returns a `true` object back to the `#all?` method, and if not it returns a `false` object back to the method. 

If at any point, the `#all?` method receives a falsy return value from the block, it will short circuit/cease iteration and return a `false` object where it was called. If, however, each return value from the block is truthy, then `#all?` will return a `true` object back to where it was called.

In this instance, since both `1` is not greater than `2`, the `#all?` method called on `line 1` will return `false` to where it was called.

(4 min)