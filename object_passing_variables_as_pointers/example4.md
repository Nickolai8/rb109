````ruby
def test(b)
  b.map {|letter| "I like the letter: #{letter}"}
end

a = ['a', 'b', 'c']
test(a)
````

This code does not display anything, but it returns An array object `["I like the letter a", "I like the letter b", "I like the letter c"]`.

On `line 5`, the local variable `a` is initialized to an array object `['a','b','c']`. On `line 6`, the `test` method is called, with the array object that local variable `a` points to used as an argument. That argument is used to initialize the `test` method parameter `b`, which now points to the same array object that the local variable `a`(which is scoped to the main method) points to/references. Inside the method definition, on `line 2`, the method parameter `b` has the `Array#map` method called on it. `Array#map` first creates a new collection, and then iterates over each element of the array, and adds the interpolated string to the new collection. After `Array#map` is done iterating, it returns the new collection back to where the method was called.

This method is a great example of how an object can be passed to a method definition via a method invocation. While local variable `a` which is scoped to the main method and `test` method parameter `b`  are not the same variable, and neither scope has access to the other variable, they both point to the same array object in memory, so `test` parameter `b` can use the array object that local variable `a` points to to call methods on.

(4-5 min)