# JDBC   (Java databse connectivity)

## What is JDBC ?
-JDBC is a Java API (Application Programming Interface) that allows Java applications to interact with relational databases (like MySQL, Oracle, PostgreSQL).

- Steps to connect Java application to database using JDBC
    - Import Packages
    - Load driver
    - Register driver
    - Create connection
    - Create statement
    - Execute statement
    - close

## Sample program to connect java application to database using JDBC


```java
import java.sql.*;

public class demojdbc {
    public static void main(String[] args) throws Exception {
        String url = "jdbc:postgresql://localhost:5432/Demo";
        String uname = "postgres";
        String pass = "1234";

        Connection con = DriverManager.getConnection(url, uname, pass);
        System.out.println("Connected to database successfully");
    }
}
