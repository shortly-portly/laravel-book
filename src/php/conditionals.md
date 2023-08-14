# Conditionals
PHP conditionals, also known as conditional statements or control structures, are used to make decisions in your code based on certain conditions. They allow you to execute different blocks of code depending on whether a specific condition is true or false. Conditional statements help control the flow of your program and enable you to create dynamic and responsive applications.

PHP provides several types of conditional statements:

1. **if Statement:**
   The `if` statement allows you to execute a block of code only if a specified condition is true.

   ```php
   $age = 25;
   
   if ($age >= 18) {
       echo "You are an adult.";
   }
   ```

2. **if-else Statement:**
   The `if-else` statement lets you execute one block of code if a condition is true and a different block of code if the condition is false.

   ```php
   $temperature = 28;
   
   if ($temperature > 30) {
       echo "It's hot outside.";
   } else {
       echo "It's not too hot.";
   }
   ```

3. **if-elseif-else Statement:**
   The `if-elseif-else` statement allows you to handle multiple conditions. It executes different blocks of code based on which condition is true.

   ```php
   $grade = 85;
   
   if ($grade >= 90) {
       echo "You got an A.";
   } elseif ($grade >= 80) {
       echo "You got a B.";
   } else {
       echo "You need to improve.";
   }
   ```

4. **switch Statement:**
   The `switch` statement is used to compare a single value against multiple possible cases. It's often used when you have many possible conditions to check.

   ```php
   $day = "Wednesday";
   
   switch ($day) {
       case "Monday":
       case "Tuesday":
       case "Wednesday":
       case "Thursday":
       case "Friday":
           echo "It's a weekday.";
           break;
       case "Saturday":
       case "Sunday":
           echo "It's a weekend day.";
           break;
       default:
           echo "Invalid day.";
   }
   ```

5. **Ternary Operator:**
   The ternary operator is a shorthand way to write simple conditional expressions. It's often used for assigning a value based on a condition.

   ```php
   $isLogged = true;
   
   $message = ($isLogged) ? "User is logged in." : "User is not logged in.";
   echo $message;
   ```

PHP conditionals are essential for making your code dynamic and responsive to different situations. They allow you to execute specific code paths based on user inputs, data, or other conditions, resulting in more flexible and interactive applications.