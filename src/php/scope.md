# Scope Resolution Operator
In PHP, the scope resolution operator (`::`) is used to access static members (properties and methods) of a class. It allows you to reference these members without needing an instance of the class. The scope resolution operator is also used to access constants defined within a class.

Here's how the scope resolution operator is used:

1. **Accessing Static Properties and Methods:**
   If a property or method in a class is declared as `static`, you can access it using the scope resolution operator. Static members belong to the class itself, not to instances of the class.

   ```php
   class MyClass {
       public static $staticProperty = "Hello, world!";
       public static function staticMethod() {
           return "This is a static method.";
       }
   }

   echo MyClass::$staticProperty; // Accessing static property
   echo MyClass::staticMethod();  // Calling static method
   ```

2. **Accessing Class Constants:**
   Class constants are accessed using the scope resolution operator as well.

   ```php
   class Math {
       const PI = 3.14159;
   }

   echo Math::PI; // Accessing a class constant
   ```

The scope resolution operator is particularly useful when you want to access shared properties, methods, or constants of a class without having to create an instance of that class. It's commonly used for utility classes, global configurations, or situations where you need to perform operations at the class level rather than on instances.