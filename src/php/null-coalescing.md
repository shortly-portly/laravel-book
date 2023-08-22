# NULL coalescing
The null coalescing operator (`??`) is a feature introduced in PHP 7 that provides a concise way to handle null values in expressions. It allows you to provide a default value when a variable is null, without the need for complex ternary operations or if-else checks.

The syntax of the null coalescing operator is:

```php
$variable = $value ?? $default;
```

In this syntax:
- `$value` is the variable you want to check for null.
- `$default` is the value to use if `$value` is null.

The null coalescing operator returns the value of `$value` if it's not null, and if it's null, it returns the value of `$default`.

Here's an example:

```php
$username = $_GET['username'] ?? 'Guest';
```

In this example, if the `$_GET['username']` parameter is set, the value of `$_GET['username']` will be assigned to `$username`. If it's not set (or is set to null), the default value `'Guest'` will be assigned to `$username`.

This operator is especially useful for providing default values in situations where you want to use a variable's value if it exists, or fall back to a default value if it's null or not set.

## NULL coalescing vs ternary operator
The null coalescing operator (`??`) and the ternary operator (`?:`) in PHP are both used to handle conditional values, but they serve different purposes and have some differences in their usage and behavior.

**Null Coalescing Operator (`??`):**
The null coalescing operator provides a convenient way to provide a default value for a variable when it's null. It's primarily used for handling cases where you want to assign a default value to a variable if it's null.

Example:
```php
$username = $_GET['username'] ?? 'Guest';
```

If `$_GET['username']` is set, `$username` will be assigned its value. If `$_GET['username']` is not set or is null, `'Guest'` will be assigned to `$username`.

**Ternary Operator (`?:`):**
The ternary operator allows you to make a decision based on a condition and choose between two values. It's used to assign one of two values to a variable based on a condition.

Example:
```php
$isLoggedIn = true;
$userStatus = $isLoggedIn ? 'Logged In' : 'Guest';
```

If `$isLoggedIn` is true, `$userStatus` will be `'Logged In'`; otherwise, it will be `'Guest'`.

**Key Differences:**
1. Purpose:
   - Null Coalescing Operator: Provides a default value if a variable is null.
   - Ternary Operator: Chooses between two values based on a condition.

2. Usage:
   - Null Coalescing Operator: Used to assign a default value to a variable if it's null.
   - Ternary Operator: Used to choose between two values based on a condition.

3. Condition:
   - Null Coalescing Operator: There's no explicit condition; it's used to check if a variable is null.
   - Ternary Operator: Requires a condition that evaluates to either true or false.

In summary, use the null coalescing operator when you want to provide a default value for a variable if it's null, and use the ternary operator when you want to choose between two values based on a condition. Both operators have their own specific use cases and can help you write more concise and readable code.
