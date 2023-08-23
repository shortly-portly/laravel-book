# Extract
The `extract()` function in PHP is used to extract variables from an associative array, turning array keys into variable names and array values into variable values. It can be a convenient way to quickly populate a set of variables with the contents of an array.

Here's the basic syntax of the `extract()` function:

```php
extract(array $array, int $flags = EXTR_OVERWRITE, string|null $prefix = null);
```

Parameters:
- `$array`: The associative array from which variables will be extracted.
- `$flags`: Optional. Specifies how to handle variable name conflicts and other options. Possible values include `EXTR_OVERWRITE`, `EXTR_SKIP`, and more.
- `$prefix`: Optional. A prefix that will be added to each extracted variable name.

Example:
```php
$data = [
    'name' => 'John',
    'age' => 30,
    'city' => 'New York'
];

extract($data);

echo $name; // Outputs: John
echo $age;  // Outputs: 30
echo $city; // Outputs: New York
```

In this example, the `extract()` function creates three variables (`$name`, `$age`, and `$city`) based on the keys of the `$data` array and assigns their corresponding values. You can then use these variables as you would with any other variables.

It's important to use `extract()` with caution, as it can make your code less readable and harder to understand if not used judiciously. When using `extract()`, keep these considerations in mind:

1. **Variable Conflicts:** Be aware of potential conflicts with existing variables or global variables when using `extract()`. You can use the `$flags` parameter to control how conflicts are handled.

2. **Naming Conventions:** Using a prefix with the `$prefix` parameter can help avoid conflicts with existing variables.

3. **Debugging:** Debugging can be more challenging when variables are created dynamically with `extract()`. Use clear and descriptive array keys to improve readability.

4. **Security:** Avoid using `extract()` with user input or untrusted data, as it can introduce security vulnerabilities if not used carefully.

In modern PHP development, the use of `extract()` is relatively rare due to its potential downsides. Instead, you might find more robust and maintainable approaches such as working directly with arrays or using objects and classes for data encapsulation.

## N.B. Laravel does not use extract() 