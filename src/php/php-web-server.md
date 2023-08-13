# PHP Built In Webserver
The `php -S` command is used to start a built-in web server for running PHP scripts without the need for a separate web server like Apache or Nginx. This feature was introduced in PHP 5.4 as a convenient way to quickly develop and test PHP applications locally.

When you run `php -S`, you're essentially starting a lightweight web server that serves PHP files and can handle requests, making it suitable for development and testing purposes. Here's how you can use it:

1. **Basic Usage:**
   To start the built-in web server, open a terminal and navigate to the root directory of your PHP application. Then run the following command:
   ```
   php -S localhost:8000
   ```
   This starts the server on `localhost` (your local machine) and listens on port `8000`. You can replace `8000` with any other available port number.

   Accessing http://localhost:8000 will attempt to serve `index.php` and, if not found, it will serve `index.html`. If it can't find `index.html` then it will return a `404` Not Found.

2. **Accessing the Application:**
   Once the server is running, you can access your PHP application by opening a web browser and navigating to `http://localhost:8000`. The server will serve the PHP files and execute them as needed.

3. **Custom Document Root:**
   By default, the server will use the current directory as the document root. If your PHP files are in a different directory, you can specify the path to that directory:
   ```
   php -S localhost:8000 -t /path/to/your/project
   ```

4. **Routing and Single-Page Applications:**
   The built-in server is also useful for single-page applications (SPAs) and routing. When you have a front-end framework that handles routing on the client side, the server can be set to serve the same HTML file for different routes. For example:
   ```
   php -S localhost:8000 -t /path/to/your/project index.php
   ```

5. **Additional Options:**
   You can run `php -S` with additional options. For example:
   - `-c` option to specify a custom php.ini file: `php -S localhost:8000 -c /path/to/php.ini`
   - `-d` option to set configuration settings: `php -S localhost:8000 -d display_errors=1`

Keep in mind that the built-in web server is intended for development and testing purposes. It's not designed to handle production traffic or provide the same level of performance and security as dedicated web servers. For production use, a more robust web server like Apache or Nginx is recommended.