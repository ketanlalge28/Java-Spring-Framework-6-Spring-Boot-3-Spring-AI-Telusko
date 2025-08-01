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
```

## TO display the Table in java
```
import java.sql.*;

public class demojdbc {
    public static void main(String[]args) throws Exception {
 String url="jdbc:postgresql://localhost:5432/Demo";
        String uname="postgres";
        String pass="1234";
        String sql="Select*from student";
        Connection con =DriverManager.getConnection(url,uname,pass);
        System.out.println("Connected to database successfully");
        Statement st=con.createStatement();
        ResultSet rs=st.executeQuery(sql);
        while(rs.next()){
            System.out.print(rs.getInt(1)+" : ");
            System.out.print(rs.getString(2)+" - ");
            System.out.println(rs.getInt(3));
        }
        con.close();
        System.out.println("Connection closed successfully");

    }
}
```
## For CRUD queries
- Insert the query which you want to execute
- Execute the statement
- syntax `st.execute(sql);`

  ## Prepared Statement
  - `PreparedStatement` is a sub-interface of `Statement` in JDBC used to execute parameterized SQL queries, which are faster, more secure, and less error-prone than regular Statement.
 
  ### ResultSet
  -A table of data representing the result of the query.

  

