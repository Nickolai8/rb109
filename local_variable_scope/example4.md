`````ruby
def example(str)
  i = 3
  loop do
    puts str
    i -= 1
    break if i == 0
  end
end

example('hello')
`````

This method displays `'hello'` to the standard output 3 times, each on its own new line. On `line 1` to `line 8`, a method named `example` is being defined as defined by `def...end`. On `line 2` inside the method, local variable `i` is initialized to the integer object `3`. `i` will be used as a counter for the upcoming loop. On `line 3`, the `loop` method is invoked with a `do..end` block attached from `line 3` to `line 7`. Inside the loop, on `line 4`, the object that the method parameter `str` references (which is whatever object is used as an argument in the method invocation. In this case, it is astring literal object `'hello'` because the `example` method is invoked on `line 10` with `'hello'` as an argument) is used as an argument to the `puts` method. The `'hello'` is displayed to the standard output, and then `nil` is returned. On `line 5`, the local variable `i` is decremented by 1. This loop runs 3 times, until the statement on `line 6`, which is `break if i == 0` is executed (at this point, local variable `i` will be decremented to 0). After this, the loop is exited, and then the method is exited as well as there is no more code inside of it. 

This code is a good example of passing objects to a method, and the method being capable of displaying those objects to the standard output. It is also yet again a good example of inner scope having access to variables that are initialized in an outer scope, since local variable `i` is accessed from inside the block attached to the `loop` method when it was initialized at `level 1` of the `example` method.



(6:15)