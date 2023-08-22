# filter_var
`filter_var` is a built-in PHP function that is used to filter and validate data based on predefined or custom filters. It's commonly used to sanitize and validate user inputs, such as form data and query parameters, to ensure they meet certain criteria and are safe to use in your application.

The `filter_var` function takes two main parameters:

1. **Value to be Filtered:** This is the data that you want to filter and validate.

2. **Filter ID or Filter Name:** This specifies the type of filter to apply to the value. PHP provides various predefined filter constants that represent different types of filters.

Here's the basic syntax of the `filter_var` function:

```php
filtered_value = filter_var(value, filter, options);
```

Example:
```php
$email = "user@example.com";
if (filter_var($email, FILTER_VALIDATE_EMAIL)) {
    echo "Valid email address.";
} else {
    echo "Invalid email address.";
}
```

In this example, `FILTER_VALIDATE_EMAIL` is a predefined filter constant that validates an email address. The `filter_var` function returns the filtered value if the input passes validation, or `false` if validation fails.

Some common predefined filter constants include:
- `FILTER_VALIDATE_EMAIL`: Validates an email address.
- `FILTER_VALIDATE_URL`: Validates a URL.
- `FILTER_SANITIZE_STRING`: Removes tags and unnecessary characters from a string.

You can also use options with some filters to further customize their behavior.

`filter_var` provides a powerful way to filter, sanitize, and validate data, helping to prevent security vulnerabilities and ensuring that the data you're working with is safe and accurate.