# Spring Framework

## Why spring framwork?
- The Spring Framework is a powerful, lightweight, and widely used open-source framework for building Java applications, especially enterprise-level applications

## Core features of spring framwork

### IOC(Inversion of Control)
- IoC in Spring is the core principle that decides how objects are created, managed, and wired together by the Spring container, instead of your application code doing it manually.


## Scope in Spring Framework
- The lifecycle and visibility of a bean.
- How many instances of the bean Spring creates and how long those instances live.

## Types of scope

### 1) Singleton
- A single shared instance of the bean for the entire Spring container.

### 2) Prototype
- A new bean instance is created every time it is requested.


### How to set value of primitive variable using xml file
- Add the property tag in the bean tag where class is linked
- In the property tag name the primitive variable and add the value
- Syntax ` <property name="variablename" value="0"> </property> `
- Example :
    ``  <bean id="alien1" class="org.example.Alien" scope="prototype">
        <property name="age" value="21"></property>
    </bean> ``

  ### Create reference attribute
 - syntax ` <property name="variablename" ref="objname"> </property> `
 - make sure that object is created in the the bean tag in xml file
   
### To add constructor
- Syntax ` <Constructor-arg index/name/type=" " value/ref=" "/>

## primary beam
- Primary bean is used when you have multiple beans of the same type and Spring needs to decide which one to inject by default.
