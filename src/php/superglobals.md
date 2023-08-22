# Superglobals
Superglobals in PHP are special arrays that are automatically available in all scopes of a script, meaning they can be accessed from any part of the script without the need to declare or import them explicitly. These arrays contain various types of data, such as form input data, server information, session data, and more.

PHP has several built-in superglobals, each serving a specific purpose:

1. **`$_GET`:**
   Contains data sent to the script via HTTP GET method (query parameters in the URL).

2. **`$_POST`:**
   Holds data sent to the script via HTTP POST method (usually from forms).

3. **`$_REQUEST`:**
   Combines `$_GET`, `$_POST`, and `$_COOKIE` data.

4. **`$_COOKIE`:**
   Holds data sent by the client's browser as cookies.

5. **`$_SESSION`:**
   Contains session data that is accessible across multiple requests for a specific user.

6. **`$_SERVER`:**
   Contains server and environment information, including headers, URLs, and paths.

7. **`$_FILES`:**
   Holds information about uploaded files via HTTP POST method (usually from forms with file inputs).

8. **`$_ENV`:**
   Holds environment variables.

9. **`$GLOBALS`:**
   Provides access to all global variables in the script's scope.

These superglobals make it easy to interact with various types of data without the need to manually process inputs or access external resources. However, it's crucial to sanitize and validate data from these superglobals before using it, especially in security-sensitive operations, to prevent security vulnerabilities like SQL injection and cross-site scripting (XSS).
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