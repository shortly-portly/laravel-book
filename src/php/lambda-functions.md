# Lambda Functions
A lambda function, also known as an anonymous function or closure, is a type of function that doesn't have a name and can be defined inline within your code. Lambda functions are useful when you need to create small, one-time-use functions without the need to explicitly declare and name them.

Lambda functions are commonly used for callbacks, filtering, sorting, and other scenarios where you want to pass a function as an argument to another function or method.

Here's the basic syntax of a lambda function in PHP:

```php
$lambdaFunction = function($param1, $param2) {
    // Function body
    return $param1 + $param2;
};
```

Here's an example of using a lambda function as a callback for the `array_map()` function:

```php
$numbers = [1, 2, 3, 4, 5];
$squared = array_map(function($num) {
    return $num * $num;
}, $numbers);

print_r($squared); // Outputs: Array ( [0] => 1 [1] => 4 [2] => 9 [3] => 16 [4] => 25 )
```

In this example, the lambda function calculates the square of each number in the array, and the `array_map()` function applies the lambda function to each element in the array.

Lambda functions can capture variables from their surrounding scope using the `use` keyword. This allows you to create closures that maintain access to variables even after they've gone out of scope.

```php
$multiplier = 2;
$calculateDouble = function($num) use ($multiplier) {
    return $num * $multiplier;
};

echo $calculateDouble(5); // Outputs: 10
```

Lambda functions are a powerful feature in PHP, enabling you to write concise and expressive code. However, they are limited to relatively simple logic due to their lack of named identifiers and visibility modifiers. For more complex scenarios, you might still want to use traditional named functions or methods.