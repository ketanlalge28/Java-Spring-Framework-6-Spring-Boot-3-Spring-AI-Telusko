# Spring Web Application


## What is Servlet?
- A Servlet is a Java program that runs on a server and handles requests from web clients (like browsers) and sends responses back.
-  It is a middleman between a browser and the server's business logic.

## What is Tomcat?
- Tomcat is a free, open-source web server and servlet container developed by the Apache Software Foundation.
- If you create a Java web application (.war file), you can deploy it on Tomcat, and Tomcat will handle all incoming HTTP requests, run your servlets/JSP, and return responses to users’ browsers.

- ## How to initialize servlet ?
- - Create a class extend the class by keyword  `HttpServlet` .
  

- ## How to initialize Tomcat ?
- - Add the depency of Tomcat in Pom.xml file.
  - Create the object of Tomcat.
  - Use `tomcat.start();` to start the tomcat.
  - Use `tomcat.getServer().await();` this method so tomcat can wait for instructions.


## MVC (Model View Controller)
- MVC is a design pattern commonly used in software development

  ### 1. Model (Simple classes or pojo classes)
  - Represents the data and the business logic of the application.
  - It directly manages the data, logic, and rules of the application.

### 2. View (JSP)
- Responsible for the UI (User Interface).
- It displays data to the user and sends user actions (like button clicks) to the controller
- These are generally HTML page, JSP, or a GUI screen

### 3. Controller (Servlet)
- Acts as a bridge between Model and View.
- It receives user input from the View, processes it (using Model), and then updates the View.
