## Java

## LTS - (Long term support)
- it means a version of Java that will receive extended updates and support from Oracle or other vendors for a longer period (typically several years). Ideal for enterprise and production use.

## How java works -
- we write java code then compiler (javac) can convert this code into byte code

- JVM (java virtual machine) can execute only byte code
  
## Method Overloading 
- same method name but has different parameters

## Stack & Heap

# Stack:
- Last in First out
- Stores local variables, references
- Smaller than heap memory
- Short term memory

# Heap
- Storing bjects, class instances and Dynamic data
-Long term memory

###Multi dimentional Array
Array of Arrays but have same length
Declaration=int arr[][]=new num[3][4]
num[3]=No of array
num[4]=Length of array

## Jagged Array
- Array of arrays can have different length for each row
- 
- It is like 2d array but has different number of elements
  

## String

# Mutable String (StringBuffer)

- A thread-safe, mutable sequence of characters.
- 
- A string buffer is like a String, but can be modified.
-  
- At any point in time it contains some particular sequence of characters, but the length and content of the sequence can be changed through certain method calls.
- 
- It supports operations like append, insert, delete, and reverse.

# Immutable String-

-String Constant Pool - this is a special memory area in Java used to store unique string literals. It helps in saving memory and improving performance by avoiding duplicate string objects.

-Both Strings s1 and s2 will point to the same object in the String Constant Pool, instead of creating two separate objects.

-you can check this with comparing this two Strings with (==) operator and .equals() method.


## Static variable
- A static variable in Java is shared among all instances of a class and is stored in memory only once.
- 
- Can be accessed using the class name or an object reference.

## Static Method
- A static method in Java belongs to the class rather than any object and can be called without creating an object.
- 
- It is declared using the static keyword and can only access static data directly (not instance variables).


## Static Block
-A static block in Java is used to initialize static variables and runs once when the class is loaded, before the main() method.


## This Keyword
- To refer current class instance variable
- 
- Useful when local variable have the same names as instance variables

## Super keyword
- super() calls a constructor from the parent class to reuse or initialize inherited properties.

 ## Final keyword - 
- Final keyword we can use with variable, method, and class.

- Final Variable: Value cannot be changed (acts as a constant).

- Final Method: Cannot be overridden by subclasses.

- Final Class: Cannot be inherited (no subclass allowed).

## Default Constructor
- A constructor that takes no parameters.
- 
- It is automatically called defined in the class.

## Parameterized Constructor
- A constructor that takes arguments/parameters.

## Difference between Final and Static keywords - 
- final makes variables constant, methods non-overridable, and classes non-inheritable.

- static makes variables and methods belong to the class, not to objects. (can access without any object).

## Wrapper class - 
- Wrapper class in Java is used to convert primitive data types into objects. Java provides a wrapper class for each primitive type, like int → Integer, char → Character, etc.

- They are useful when:

    - Working with collections like ArrayList (which only store objects),

    - Using utility methods (e.g., Integer.parseInt()),
 
## Dynamic Method Dispatch - 
- Dynamic Method Dispatch in Java is the process where the method call is resolved at runtime, not compile time.
- It occurs when a parent class reference points to a child class object, and the overridden method in the child class gets called. 
- This enables runtime polymorphism, allowing Java to decide which method to execute based on the actual object.
