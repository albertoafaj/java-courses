# Persistent Storage of Data

In Java, persistent storage of data can be achieved using a relational database management system (RDBMS) such as MySQL, Oracle, or PostgreSQL.

To work with a database in Java, you can use a JDBC (Java Database Connectivity) driver to establish a connection to the database and execute SQL statements. Here's an example of persisting data in a MySQL database using JDBC:

```

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import java.sql.SQLException;

public class UserDAO {
    private final String url = "jdbc:mysql://localhost:3306/mydb";
    private final String user = "root";
    private final String password = "password";

    public void addUser(User user) {
        String sql = "INSERT INTO users (id, name, email) VALUES (?, ?, ?)";

        try (Connection conn = DriverManager.getConnection(url, user, password);
             PreparedStatement pstmt = conn.prepareStatement(sql)) {

            pstmt.setInt(1, user.getId());
            pstmt.setString(2, user.getName());
            pstmt.setString(3, user.getEmail());

            pstmt.executeUpdate();
        } catch (SQLException e) {
            System.out.println(e.getMessage());
        }
    }
}

```

In this example, we define a UserDAO class that contains a method addUser() that takes a User object as an argument and adds it to a MySQL database.

We first define the connection details for the database using a URL, username, and password.

We then define an SQL INSERT statement that inserts a new row into the users table, with placeholders for the id, name, and email fields.

We establish a connection to the database using the getConnection() method of the DriverManager class.

We then create a PreparedStatement object with the SQL statement, and set the values of the placeholders using the setter methods of the PreparedStatement object.

We then execute the SQL statement using the executeUpdate() method of the PreparedStatement object.

If there is any error during this process, we catch the SQLException and print the error message to the console.

This is just a simple example, but it demonstrates the basic concepts of persisting data in a relational database using Java and JDBC. In practice, you would typically define a DAO (Data Access Object) layer that handles all database interactions, and use ORM (Object-Relational Mapping) frameworks such as Hibernate or JPA to simplify database interactions and mapping of objects to database tables.

### Step-by-step basic connection

1. Add the JDBC driver to your project's classpath:

Download the JDBC driver for your database management system and add it to your project's classpath. This can be done by copying the driver JAR file to your project's lib directory and adding it to the classpath in your build system configuration.

2. Load the JDBC driver class:

Load the JDBC driver class using the Class.forName() method, passing the fully qualified class name of the driver as a string. For example, to load the MySQL JDBC driver, you would call:

``` 
Class.forName("com.mysql.jdbc.Driver");
```

3. Establish a connection to the database:

Create a Connection object by calling the DriverManager.getConnection() method and passing in the URL, username, and password for your database. For example, to connect to a MySQL database, you would call:

```
String url = "jdbc:mysql://localhost/mydatabase";
String username = "myusername";
String password = "mypassword";
Connection conn = DriverManager.getConnection(url, username, password);
```

4. Create a statement or prepared statement:

Create a Statement or PreparedStatement object that will be used to execute SQL queries and commands. A Statement object is used to execute a static SQL statement, while a PreparedStatement object is used to execute a SQL statement that may have input parameters. For example, to create a PreparedStatement object to execute a parameterized SQL query, you would call:

```
String sql = "SELECT * FROM mytable WHERE id = ?";
PreparedStatement pstmt = conn.prepareStatement(sql);
pstmt.setInt(1, 1);
```

5. Execute the SQL query or command:

Use the execute() or executeUpdate() method of the Statement or PreparedStatement object to execute the SQL query or command. For example, to execute a SQL query and retrieve the results, you would call:

```
String sql = "SELECT * FROM mytable";
ResultSet rs = stmt.executeQuery(sql);
while (rs.next()) {
    // process each row of the result set
}
```

6. Close the statement and connection:

Close the Statement, PreparedStatement, and Connection objects when you are finished using them. This can be done by calling their close() method in a finally block. For example:

```
try {
    // execute SQL statements
} catch (SQLException e) {
    // handle exceptions
} finally {
    if (rs != null) rs.close();
    if (stmt != null) stmt.close();
    if (conn != null) conn.close();
}
```

That's it! This is a basic guide to connect to a database using JDBC in Java. Keep in mind that this is just the beginning, and there are many more things to learn about JDBC, such as connection pooling, transactions, and more advanced SQL queries.