# Rest Using Spring Boot

## REST(Representational State Transfer)
- It is an architectural style for building web services that communicate over HTTP.

### Common HTTP Methods in REST
| HTTP Method | Meaning                   | Example                                        |
| ----------- | ------------------------- | ---------------------------------------------- |
| **GET**     | Read data                 | `GET /users` → Get all users                   |
| **POST**    | Create new resource       | `POST /users` → Add a new user                 |
| **PUT**     | Update entire resource    | `PUT /users/1` → Update user with ID=1         |
| **PATCH**   | Update part of a resource | `PATCH /users/1` → Update only email of user 1 |
| **DELETE**  | Delete a resource         | `DELETE /users/1` → Delete user 1              |


### What is ORM & JPA?

ORM = Object Relational Mapping
- It’s a technique to map Java objects (classes) to relational database tables.
- Instead of writing SQL queries directly, you work with Java objects, and the ORM tool takes care of translating those operations into SQL.

JPA = Java Persistence API
- It is a specification (a set of rules/interfaces) for ORM in Java.
- JPA itself does not provide implementation.
- It just defines how ORM should work in Java applications.
