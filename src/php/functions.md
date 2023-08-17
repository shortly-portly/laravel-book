# Functions
In PHP, a function is a self-contained block of code that performs a specific task. Functions allow you to encapsulate code logic, make your code more modular and organized, and avoid redundancy by reusing the same code in multiple places. Functions are a fundamental concept in programming and play a crucial role in writing maintainable and efficient code.

Here's how you define and use functions in PHP:

1. **Function Declaration:**
   You define a function using the `function` keyword, followed by the function name, a set of parentheses, and a code block enclosed in curly braces. The code inside the block represents the task the function performs.

   ```php
   function greet() {
       echo "Hello, world!";
   }
   ```

2. **Function Parameters:**
   Functions can accept parameters, which are variables passed to the function when it's called. Parameters allow you to provide dynamic data to the function for processing.

   ```php
   function sayHello($name) {
       echo "Hello, $name!";
   }
   ```

3. **Function Return Values:**
   Functions can also return values after performing their task. The `return` statement is used to specify the value to be returned.

   ```php
   function add($a, $b) {
       return $a + $b;
   }
   ```

4. **Calling Functions:**
   To use a function, you call it by its name followed by parentheses. If the function has parameters, you provide the values for those parameters in the parentheses.

   ```php
   greet(); // Outputs: Hello, world!
   sayHello("Alice"); // Outputs: Hello, Alice!
   $result = add(5, 3); // $result will contain 8
   ```

Functions provide several benefits, including:

- **Code Reusability:** Functions allow you to write code once and use it multiple times in different parts of your program.
- **Modularity:** Breaking down your code into functions makes it more organized and easier to maintain.
- **Abstraction:** Functions abstract away the implementation details, allowing you to use a function without needing to know how it works internally.
- **Readability:** Well-named functions can make your code more readable and understandable.

PHP has a vast collection of built-in functions, and you can also create your own custom functions to suit your specific application needs.

## Default Parameters
In a PHP function, a default parameter (also known as a default argument) is a value that you can assign to a parameter when defining the function. If a value is not provided for that parameter when the function is called, the default value will be used instead.

Default parameters are particularly useful when you want to provide a sensible or common value for a parameter while still allowing the flexibility to override that value when necessary.

Here's the basic syntax for defining a function with default parameters:

```php
function myFunction($param1, $param2 = defaultValue) {
    // Function body
}
```

In this example, `$param2` is a parameter with a default value of `defaultValue`. If you don't provide a value for `$param2` when calling the function, it will automatically take on the value of `defaultValue`.

Here's a practical example:

```php
function greet($name, $greeting = "Hello") {
    echo "$greeting, $name!";
}

greet("Alice");         // Outputs: Hello, Alice!
greet("Bob", "Hi");     // Outputs: Hi, Bob!
```

In the `greet()` function, the `$greeting` parameter has a default value of `"Hello"`. If you don't provide a second argument when calling the function, it will default to `"Hello"`. However, you can override the default value by passing a different value explicitly.

Default parameters help make functions more flexible and user-friendly by allowing you to define sensible default behavior while still accommodating customization when needed. They are especially useful when you want to provide backward compatibility for existing code that relies on older function signatures.