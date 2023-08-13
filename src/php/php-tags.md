# PHP Tags
`<?php` is the opening tag used in PHP to indicate the beginning of PHP code within an HTML or text document. It tells the PHP interpreter that the subsequent content should be treated as PHP code and should be processed accordingly.

When the PHP interpreter encounters `<?php`, it switches from parsing regular HTML or text to interpreting PHP instructions. Here's how it's typically used within an HTML context:

```html
<!DOCTYPE html>
<html>
<head>
    <title>PHP Example</title>
</head>
<body>
    <h1><?php echo "Hello, World!"; ?></h1>
    <p>This is a PHP example.</p>
</body>
</html>
```

In the example above, the `<?php echo "Hello, World!"; ?>` code within the `<h1>` tag is PHP code that will be executed on the server when the page is requested. The output of the PHP code ("Hello, World!") will be inserted into the HTML document that is sent to the browser, resulting in the displayed output:

```html
<!DOCTYPE html>
<html>
<head>
    <title>PHP Example</title>
</head>
<body>
    <h1>Hello, World!</h1>
    <p>This is a PHP example.</p>
</body>
</html>
```

In summary, `<?php` is used to indicate the start of PHP code within an HTML or text file, allowing you to dynamically generate content and interact with databases, files, and other server-side resources.