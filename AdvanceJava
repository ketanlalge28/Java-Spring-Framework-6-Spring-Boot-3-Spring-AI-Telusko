
# Advance java


## Abstract class - 
- A class that cannot be directly instantiated.

- Contains abstract methods (no body) and/or concrete methods.

- Meant to be extended by subclasses.

- Can be instantiated using an anonymous inner class by providing method implementations on the spot.




## Inner class - 
- An inner class in Java is a class defined inside another class. 
- It helps logically group classes and can access all members of the outer class, even private ones. 
- Inner classes are mainly used to make code more readable and organized. 
- There are different types like regular, static, local, and anonymous inner classes.

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

## Lambda Expression - 
- A lambda expression in Java is a concise way to represent an anonymous function. 
- It is used mainly to implement functional interfaces (interfaces with a single abstract method). 
- Introduced in Java 8, it helps reduce boilerplate code, especially in collections and stream operations. Example: `(a, b) -> a + b`.

## Exception - 
- An exception is a problem (error) that happens while the program is running. 

- For example, if you try to divide a number by zero, access an invalid array index, or open a file that doesn't exist — Java throws an exception.

- Instead of crashing the program, Java allows you to handle these problems using special code.

## `try` - `catch` block - 
- The try-catch block is used to handle exceptions. 

- You write the risky code (the code that might cause an exception) inside the try block. 

- If an exception happens, the code inside the catch block runs.

- `try`: Contains the code that may cause an exception.

- `catch`: Catches the exception and lets you write code to handle the error.

- You can also write `try` without `catch` but ensure that you have `finally`.

- One of them is necessary with `try` to avoid the compile time error but one thing keep in mind that without catch you cannot handle exception.


## `throw` keyword -
- The `throw` keyword is used to manually throw an exception in your code.


- Use throw when you want to create and throw an exception yourself.

- We usually write `throw` inside the `try` block, because when we manually throw an exception, we also want to catch it and handle it properly.


## `throws` keyword - 
- The `throws` keyword is used in method declarations to say that this method might throw an exception.

- if a method can cause an exception, you use throws to warn the CALLER to handle it.


## `finally` block - 
- The finally block always runs after try-catch, whether an exception happens or not. 

- It is used for cleanup work, like closing files or database connections.


## Custom Exception - 
- You can create your own exception class to represent specific problems in your application that aren't covered by built-in exceptions.

- A custom exception in Java is a user-defined error type that extends the Exception or RuntimeException class

## BufferedReader and InputStreamReader - 
- `BufferedReader` needs a Reader object — and `InputStreamReader` is a Reader.

- So we combine them to read user input from console (System.in) efficiently. 

- ex.
    -   -> BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

    -   -> String input = br.readLine();  // reads a full line from keyboard


## Thread - 
- A thread in Java is a lightweight unit of execution.
- It is like a small part of a program that runs independently and in parallel with other threads.
- ### Multithread - 
    - Multithreading means running two or more threads at the same time in a program.
    - Each thread runs independently and does its own task in parallel.


- ### Thread priority - 
    - Thread priority decides which thread is more important for the CPU.
    - Java threads can have a priority value from 1 to 10.

- ### Thread sleep - 

    - `Thread.sleep(milliseconds)` pauses the current thread for the given time.

- ### What is Thread class?
    - Thread is a built-in Java class that represents a thread of execution.
    - You can create a thread by extending the Thread class and overriding its run() method.

- ### What is Runnable interface?

    - Runnable is a functional interface with a single method: run().
    - Instead of extending a class, you implement this interface and pass it to a Thread object.

- ### What is a Race Condition?

    - A race condition is a problem that happens when two or more threads access shared data at the same time, and the final result depends on the order in which threads run.

    - It leads to unexpected or incorrect behavior.
    - Ex. Imagine two people trying to edit the same file at the same time. If they both make changes without coordinating, the file may end up in a corrupt or wrong state. That’s a race condition.

- ### What is thread states? 
    - A thread in Java goes through various states during its life cycle, like:

    - New

    - Runnable

    - Running

    - Blocked

    - Waiting / Timed Waiting

    - Terminated (Dead)


## Collection -
- A Collection is an object that can hold multiple elements together, like a list of names, a set of IDs, or a map of key-value pairs.

- #### Collection :
    - List -
        - Arraylist 
            - An ArrayList is a resizable array (also called dynamic array) in Java.
            - It is part of the java.util package and implements the List interface.
            - `import java.util.ArrayList`
            - `ArrayList<Type> listName = new ArrayList<>();`
        - Linkedlist
    - Set -
        - Hashset
            - A HashSet is a class in Java that implements the Set interface and is used to store a collection of unique elements (i.e., no duplicates allowed).

            - It is part of the java.util package and internally uses a HashMap for storage.

            - `import java.util.HashSet;`

            - `HashSet<Type> setName = new HashSet<>();`

        - LinkedHashset
    - Queue - 
        - Dequeue



 - #### Collection API :
    - Map -
        - HashMap
        - HashTable
        


## Comparator vs Comparable - 
- `Comparable` and `Comparator` are interfaces used for sorting objects.
- They define how objects should be compared when sorting or ordering collections like `ArrayList`, `TreeSet`, etc.

- If you want to write your own logic to sort then you can use `Comparator`

- If you want to give power to class to compare its objects itself, we can use `Comparable` there.



## forEach method - 
- In Java, the .forEach() method is used to iterate over elements in a collection such as a List, Set, or Map using lambda expressions or method references. 
- It is available from Java 8 onwards as part of the Iterable interface and the Streams API.
- Simply we can use this to print the items of different data structure.

- ex.   
    `List<String> names = Arrays.asList("Alice", "Bob", "Charlie");`

    `names.forEach(name -> System.out.println(name));`


## Stream - 
- A Stream is a sequence of elements that supports functional-style operations to process data, such as filtering, mapping, sorting, etc., without modifying the original data source.
- `List<String> names = Arrays.asList("Alice", "Bob", "Charlie");`

    `names.stream()
    .filter(name -> name.startsWith("A"))
     .forEach(System.out::println);`

## Parallel Stream - 
- `parallelStream()` is a way to process streams concurrently, using multiple CPU threads automatically, ideal for large, performance-critical tasks where the order of processing does not matter.



















# Revisit this topics : 
- ## Thread
- ## Stream
- ## Parallel Stream
- ## Optional class in Java
- ## Method Reference
- ## Constructor Reference
