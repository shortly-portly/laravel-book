# Variables
In PHP, variables are used to store and manipulate data. They act as placeholders for various types of information, such as numbers, strings, arrays, and objects. Variables enable you to store values and use them throughout your code, making your PHP scripts dynamic and flexible. Here's how you declare and use variables in PHP:

1. **Variable Declaration:**
   In PHP, you declare a variable by using the dollar sign `$` followed by the variable name. Variable names must start with a letter or underscore (`_`), followed by letters, numbers, or underscores. They are case-sensitive, meaning `$myVar` and `$myvar` are considered different variables.

   ```php
   $name = "John";
   $age = 30;
   $pi = 3.14;
   $isStudent = true;
   ```

2. **Assigning Values:**
   You assign values to variables using the assignment operator `=`. The value can be a constant, a result of an expression, or the return value of a function.

   ```php
   $count = 5;
   $total = $price * $quantity;
   ```

3. **Variable Types:**
   PHP is loosely typed, which means you don't need to declare the data type of a variable explicitly. PHP automatically assigns the appropriate data type based on the value you assign to the variable.

4. **Variable Interpolation:**
   When using variables in double-quoted strings, you can directly insert their values using variable interpolation.

   ```php
   $name = "Alice";
   echo "Hello, $name!"; // Output: Hello, Alice!
   ```

5. **Variable Scope:**
   The scope of a variable defines where it can be accessed. Variables can be global (accessible throughout the script) or local (only within a specific function or code block).

6. **Dynamic Typing:**
   PHP variables can change data types during runtime. For example, you can assign an integer value to a variable and later assign a string to the same variable without any issues.

7. **Variable Concatenation:**
   When working with strings, you can concatenate (combine) variables and strings using the `.` operator.

   ```php
   $firstName = "John";
   $lastName = "Doe";
   echo "Full name: " . $firstName . " " . $lastName; // Output: Full name: John Doe
   ```

Variables are a fundamental concept in programming, including PHP. They allow you to store and manipulate data dynamically, making your code more versatile and capable of adapting to changing situations.