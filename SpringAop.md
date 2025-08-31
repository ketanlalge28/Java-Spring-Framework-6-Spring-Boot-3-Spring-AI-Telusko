## Spring Aop
- Spring AOP (Aspect-Oriented Programming) is a powerful feature of the Spring Framework that allows you to separate cross-cutting concerns (like logging, security, transactions, performance monitoring, etc.) from the main business logic of your application.

 ### When to Use Spring AOP?
- Logging
- Security checks (authentication/authorization)
- Transaction management
- Performance monitoring (execution time)
- Exception handling

## Terminologies of AOP
- Aspect: A module that encapsulates behaviors affecting multiple
classes.
- Join Point: A point in the execution of a program, such as method
execution or exception handling.
- Advice: The action taken by an aspect at a particular join point (e.g.,
@Before, @After).
- Pointcut: The expression that defines at which join points advice
should be applied.
- Target: The object being advised by one or more aspects.
- AOP Proxy: A proxy object created by the AOP framework.
- Weaving: The process of linking aspects with other application types.
