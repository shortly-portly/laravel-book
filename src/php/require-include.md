# Require vs Include
Both `require` and `include` are used to include external files into your PHP script. These files can contain functions, classes, variables, or any other PHP code that you want to reuse across multiple scripts. The primary difference between `require` and `include` lies in how they handle errors and the consequences of those errors.

1. **require:**
   The `require` statement is used to include a file in your script. If the file is not found or encounters an error, PHP will generate a fatal error and halt the script's execution.

   ```php
   require 'myfile.php'; // Include the file

   // Code after the require statement
   ```

   If `myfile.php` cannot be found or contains an error, the script will stop running, and you'll see an error message on the screen.

2. **include:**
   The `include` statement is also used to include a file in your script. However, if the file is not found or encounters an error, PHP will generate a warning and continue executing the script.

   ```php
   include 'myfile.php'; // Include the file

   // Code after the include statement
   ```

   If `myfile.php` cannot be found or contains an error, the script will continue to run, but you might see a warning message indicating that the included file could not be processed.

In summary:

- Use `require` when you want the included file to be absolutely necessary for your script's functionality. If the file is missing or contains errors, it will halt the script.
- Use `include` when you want the included file to enhance your script but not necessarily stop the script if there's an issue with the file.

Additionally, there are variants called `require_once` and `include_once`. These work the same as their non-"once" counterparts, but they ensure that the file is included only once even if you attempt to include it multiple times in different parts of your script. This is useful to avoid redefining functions or variables multiple times.

```php
require_once 'myfile.php'; // Include the file only once
include_once 'myfile.php'; // Include the file only once
```

Choosing between `require` and `include` depends on the level of importance and dependency of the included file in your script.