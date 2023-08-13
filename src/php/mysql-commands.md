# Useful Commands

1. **Connecting to MySQL:**
   - `mysql -u username -p`: Opens a MySQL command-line interface, prompting for the password of the specified user.

2. **Database Operations:**
   - `CREATE DATABASE database_name;`: Creates a new database.
   - `USE database_name;`: Selects a database to work with.
   - `SHOW DATABASES;`: Lists all available databases.
   - `DROP DATABASE database_name;`: Deletes a database (be cautious with this command, as it permanently removes the database and its data).

3. **Table Operations:**
   - `CREATE TABLE table_name (column1 datatype, column2 datatype, ...);`: Creates a new table with specified columns and data types.
   - `SHOW TABLES;`: Lists all tables in the currently selected database.
   - `DESCRIBE table_name;` or `DESC table_name;`: Displays the structure of a table, showing its columns, data types, and other attributes.
   - `DROP TABLE table_name;`: Deletes a table (similar caution applies here as with dropping databases).

4. **Data Manipulation:**
   - `INSERT INTO table_name (column1, column2, ...) VALUES (value1, value2, ...);`: Inserts data into a table.
   - `SELECT * FROM table_name;`: Retrieves all data from a table.
   - `SELECT column1, column2 FROM table_name WHERE condition;`: Retrieves specific columns' data based on a condition.
   - `UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;`: Updates data in a table.
   - `DELETE FROM table_name WHERE condition;`: Deletes data from a table.

5. **Querying and Filtering:**
   - `SELECT * FROM table_name WHERE column_name = value;`: Retrieves rows that match a specific condition.
   - `SELECT * FROM table_name ORDER BY column_name ASC/DESC;`: Retrieves rows sorted in ascending (ASC) or descending (DESC) order based on a column.
   - `SELECT DISTINCT column_name FROM table_name;`: Retrieves unique values from a specific column.

6. **Aggregation and Functions:**
   - `SELECT COUNT(*) FROM table_name;`: Retrieves the count of rows in a table.
   - `SELECT AVG(column_name) FROM table_name;`: Retrieves the average value of a numeric column.
   - `SELECT SUM(column_name) FROM table_name;`: Retrieves the sum of values in a numeric column.
   - `SELECT MAX(column_name) FROM table_name;`: Retrieves the maximum value from a column.
   - `SELECT MIN(column_name) FROM table_name;`: Retrieves the minimum value from a column.

Remember that these commands are executed within the MySQL command-line interface or other MySQL client tools. It's essential to be cautious when using commands that modify or delete data, especially in a production environment, as these actions can't be undone. Always ensure you have backups and are running in a controlled environment.