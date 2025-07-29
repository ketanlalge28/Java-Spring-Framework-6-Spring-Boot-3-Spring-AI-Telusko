# Advance Java


## Abstract Keyword
   -An abstract method is a method that does not have a body. It must be overridden in a subclass.

## Abstract class - 
- A class that cannot be directly instantiated.

- Contains abstract methods (no body) and/or concrete methods.

- Meant to be extended by subclasses.

- Can be instantiated using an anonymous inner class by providing method implementations on the spot.

## Inner Class-
- Inner Class is a Class inside class
- It helps logically group classes and can access all members of the outer class, even private ones. 
- Inner classes are mainly used to make code more readable and organized. 
- Syntax to call inner class method
-  `A.B obj1=obj.new B();`
- By declaring static class
- `A.B obj1=new A.B(); `

  ## Anonymous inner class -
- An anonymous inner class is a type of inner class without a name, declared and instantiated in a single statement. 
- It is used when you need to override a method of a class or interface only once, usually for short-term use like event handling.

## Interface - 
- An interface in Java is a blueprint for a class that defines abstract methods (no body).
- It is used to specify what a class must do, but not how it does it.
- By default Interface methods have method type 'public void', no need to specify method type.
- Interface can have only static or final variables.
- Interface don't have separate memory in heap.
- Types of interfaces - 
    - Normal 
    - Functional (single abstract method)
    - Marker

## Enum - 
- An enum in Java is a special data type used to define a fixed set of constant values (like days, directions, etc.). 
- It improves type safety and makes code more readable. 
- Enums can also have fields, methods, and constructors. They are declared using the enum keyword.
- Enum cannot be inherit into another class.

## Annotations - 
- Annotations in Java are special metadata tags used to provide information to the compiler or runtime. 
- They do not affect program logic but help tools, frameworks, or the compiler understand how to process code. 
- Common examples include `@Override`, `@Deprecated`, and `@SuppressWarnings`. You can also create custom annotations.
