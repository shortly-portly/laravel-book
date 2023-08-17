# Superglobals
Yes, you can pass variables to a partial when including it in PHP. This is a common practice that allows you to populate the partial with dynamic data based on the context of the page. Passing variables to partials is useful for creating reusable components that can display different content based on the values you provide.

Here's how you can pass variables to a partial:

1. **Create the Partial File:**
   Start by creating a partial file containing HTML and placeholders for the variables.

   ```php
   <!-- partial.php -->
   <div class="user-profile">
       <h2><?php echo $username; ?></h2>
       <p>Email: <?php echo $email; ?></p>
   </div>
   ```

2. **Include the Partial with Variables:**
   When you include the partial, make sure to define the variables before including it.

   ```php
   <!-- main.php -->
   <!DOCTYPE html>
   <html>
   <head>
       <title>User Profile</title>
   </head>
   <body>
       <?php
       $username = "JohnDoe";
       $email = "john@example.com";
       include 'partial.php';
       ?>
   </body>
   </html>
   ```

In this example, the variables `$username` and `$email` are defined in the `main.php` file. When the `partial.php` file is included, it can access and display the values of these variables within its HTML structure.

This approach allows you to reuse the same partial template for different users with different data. You can also pass arrays, objects, or any other data type as variables to a partial, depending on your needs.

Remember that when you include a file that uses variables, those variables are in the same scope as the including file. Therefore, they can be accessed within the included partial without any additional steps.

Using variables in partials adds flexibility and dynamism to your reusable components, making them adaptable to different contexts and data sources.

## Displaying Superglobals

Using `var_dump()` with the `<pre>` tag is a common practice to improve the readability of the output. When you wrap the `var_dump()` output in a `<pre>` tag, the output will be displayed in a preformatted block, which preserves line breaks and indentation. This can make the output much more organized and easier to understand, especially when dealing with complex data structures.

Here's how you can use `var_dump()` with the `<pre>` tag:

```php
echo '<pre>';
var_dump($_GET);
echo '</pre>';
```

By enclosing the `var_dump()` output in `<pre>` tags, the array structure, data types, and values will be displayed in a nicely formatted way, making it easier to analyze the content.

You can apply this technique to any variable or data structure you want to inspect, not just superglobals. It's particularly useful when debugging and analyzing arrays, objects, and other complex data.

Keep in mind that using `var_dump()` and `<pre>` is typically used during development and debugging. In a production environment, you may want to avoid showing such detailed information to end users.

Here's an example of using `var_dump()` with the `<pre>` tag to display the content of the `$_GET` superglobal:

```php
echo '<pre>';
var_dump($_GET);
echo '</pre>';
```

Assuming you have a URL like `http://example.com/index.php?name=John&age=30`, the output might look like this:

```
array(2) {
  ["name"]=>
  string(4) "John"
  ["age"]=>
  string(2) "30"
}
```

In this example, the `<pre>` tag preserves the line breaks and indentation from the `var_dump()` output, making it easier to read and understand the structure of the `$_GET` array. The output indicates that the `$_GET` array contains two key-value pairs: `"name"` with the value `"John"` and `"age"` with the value `"30"`.

Using the combination of `var_dump()` and the `<pre>` tag is a helpful technique for debugging and understanding the content of variables, arrays, and objects in PHP.