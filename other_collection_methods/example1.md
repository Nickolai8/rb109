````ruby
[1, 2, 3].any? do |num|
  num > 2
end
````

On `line 1`, the array object `[1,2,3]` has the `Array#any?` method called on it. The `#any?` method iterates over each index position of the array object that it was called on, and yields the element object in the current index position over to the block as an argument in order to initialize the block parameter, which is `num`.

During each block iteration, the object that `num` references is compared to the integer object `2`. If the object that `num` references has a higher numerical value than `2`, then the block returns a `true` object to the `#any?` method. If not, it returns a `false` object to the method.

If at any point, `#any?` receives a truthy value from the block that is attached to it, it will short circuit/cease to keep iterating, and return a `true` object to where the method was called. If however, no truthy block value is returned, `#any?` will return a `false` object to where it was called.

This code is a good example of how the method `#any?` works.

(2.5-3 min).

