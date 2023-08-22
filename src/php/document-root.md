# Document Root
In web development, the term "document root" refers to the directory on a web server where the main content of a website is stored. It's the top-level directory from which web server software serves files in response to HTTP requests. When a user requests a specific URL, the web server looks in the document root to find the corresponding file or resource to send back to the user's browser.

The document root is the starting point for accessing files and resources through a web browser. It's also known as the "web root" or "web directory." The files in the document root are accessible to users when they navigate to the website's domain or subdomain.

For example, if the document root is set to `/var/www/html` on a web server, and a user navigates to `http://example.com`, the web server will serve files from the `/var/www/html` directory.

The document root is an important concept in web hosting and server configuration, as it determines where website files are located on the server's filesystem and how they are accessed by visitors. It's also a key consideration when setting up server security to prevent unauthorized access to sensitive files.

In the context of PHP, the document root is often used to specify the path to files that are publicly accessible via a web browser, such as HTML, CSS, JavaScript, and image files. It's also used to determine the location from which PHP scripts can be executed by the web server.

## why should you not put your files in document root

Putting sensitive files directly in the document root of a web server is generally not recommended due to security concerns. Here are some reasons why you should avoid placing files directly in the document root:

1. **Exposure of Sensitive Information:** Placing sensitive files, such as configuration files containing database credentials or other sensitive data, in the document root could expose them to unauthorized access. Malicious users may attempt to access these files and gain access to critical information.

2. **Direct Access to Source Code:** Placing source code files, such as PHP files, directly in the document root might expose your application's logic and code to anyone who can access them. This can be a security risk, as attackers could potentially identify vulnerabilities or exploit weaknesses in your code.

3. **Unintended Public Access:** If files are placed in the document root unintentionally or without proper access controls, they could become publicly accessible. This might lead to data exposure or unauthorized modification of files.

4. **Reduced Control:** Placing files directly in the document root might make it harder to manage access control and permissions. Using a separate directory structure allows for finer-grained control over which files are accessible and who can access them.

5. **Security Hardening:** Placing files outside the document root enables security measures like access restrictions and URL rewriting to be more effective in protecting your application.

To address these concerns, it's recommended to structure your web application's files in a way that separates sensitive and non-public files from those that are meant to be accessed by users. Consider using the following approach:

1. **Use a Non-Web-Accessible Directory:** Place sensitive files, configuration files, and source code outside the document root in a directory that is not directly accessible via a URL.

2. **Implement Access Control:** Use server-side configurations (like `.htaccess` files for Apache) to control access to specific directories and files. This prevents direct access to sensitive files.

3. **Code Organization:** Organize your codebase so that only files that need to be accessed by users are located within the document root. Keep business logic, configuration, and sensitive files outside of the document root.

4. **Secure File Permissions:** Ensure proper file and directory permissions are set to limit who can read, write, or execute files. Avoid using overly permissive permissions.

By adopting these practices, you can enhance the security of your web application and reduce the risk of exposing sensitive information or vulnerabilities to potential attackers.

## what are best practises with document root and php

When working with the document root and PHP, there are several best practices you should follow to ensure the security, organization, and performance of your web applications. Here are some recommended practices:

1. **Secure Directory Structure:**
   - Keep sensitive files, configuration files, and source code outside of the document root to prevent direct access.
   - Organize your codebase with a clear separation between public files (accessible via the web) and private files (not accessible via the web).

2. **Use Frameworks and Libraries:**
   - Utilize PHP frameworks like Laravel, Symfony, or Yii that provide built-in security features, routing, and templating systems.
   - Use reputable libraries for common tasks like database interactions, authentication, and input validation.

3. **Input Validation and Sanitization:**
   - Always validate and sanitize user inputs to prevent security vulnerabilities like SQL injection and cross-site scripting (XSS).

4. **Avoid Mixing Logic with Presentation:**
   - Separate your business logic from your presentation layer using the MVC (Model-View-Controller) or similar design patterns.

5. **Use Prepared Statements:**
   - When interacting with databases, use prepared statements and parameterized queries to prevent SQL injection attacks.

6. **Escape Output:**
   - Use output escaping (e.g., `htmlspecialchars`) to prevent XSS attacks when displaying user-generated content.

7. **Secure Configuration:**
   - Store sensitive configuration data (such as database credentials) in environment variables or secure configuration files outside of the document root.

8. **File Uploads:**
   - Store uploaded files outside the document root or in a designated directory with strict access controls.
   - Validate and sanitize uploaded file names and types to prevent malicious uploads.

9. **Error Handling and Logging:**
   - Implement proper error handling and logging mechanisms to capture and handle application errors.
   - Avoid showing detailed error messages to users in production environments.

10. **Use HTTPS:**
    - Use HTTPS to encrypt data transmission between the server and clients, protecting sensitive information from interception.

11. **Regular Updates:**
    - Keep your PHP version, web server, and any third-party libraries up to date to benefit from security patches.

12. **Secure Third-Party Code:**
    - Be cautious when using third-party code or plugins. Ensure they come from reputable sources and are regularly updated.

13. **Server Configuration:**
    - Secure your server by configuring access controls, firewalls, and intrusion detection systems.

14. **Backup and Recovery:**
    - Regularly back up your website's files and database to ensure you can recover from unexpected issues.

15. **Content Security Policy (CSP):**
    - Implement a CSP to control which external resources can be loaded by your web application, reducing the risk of XSS attacks.

By following these best practices, you can create secure, maintainable, and efficient PHP web applications while minimizing the risk of security vulnerabilities and performance issues.