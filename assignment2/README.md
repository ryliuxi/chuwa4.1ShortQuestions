1. What is Interface and what is abstract class? What are the differences between them?

Both abstract class and interface are used for abstraction.

The interface is a blueprint that can be used to implement a class. The interface does not contain any concrete methods (methods that have code). All the methods of an interface are abstract methods.

An interface cannot be instantiated. However, classes that implement interfaces can be instantiated. Interfaces never contain instance variables but, they can contain public static final variables (i.e., constant class variables)


A class which has the abstract keyword in its declaration is called abstract class. Abstract classes should have at least one abstract method. , i.e., methods without a body. It can have multiple concrete methods.

Abstract classes allow you to create blueprints for concrete classes. But the inheriting class should implement the abstract method.

Abstract classes cannot be instantiated.


https://www.guru99.com/interface-vs-abstract-class-java.html#:~:text=An%20abstract%20class%20permits%20you,class%20can%20implement%20multiple%20interfaces.



2.  What is the differences between overriding and overloading?

## What is Overloading and Overriding?
When two or more methods in the same class have the same name but different parameters, it’s called Overloading.

When the method signature (name and parameters) are the same in the superclass and the child class, it’s called Overriding.

## Overriding vs Overloading

Overriding implements Runtime Polymorphism whereas Overloading implements Compile time polymorphism.
The method Overriding occurs between superclass and subclass. Overloading occurs between the methods in the same class.
Overriding methods have the same signature i.e. same name and method arguments. Overloaded method names are the same but the parameters are different.
With Overloading, the method to call is determined at the compile-time. With overriding, the method call is determined at the runtime based on the object type.

If overriding breaks, it can cause serious issues in our program because the effect will be visible at runtime. Whereas if overloading breaks, the compile-time error will come and it’s easy to fix.


https://www.journaldev.com/32182/overriding-vs-overloading-in-java#:~:text=What%20is%20Overloading%20and%20Overriding,child%20class%2C%20it's%20called%20Overriding.


3.  What is final key word? (Filed, Method, Class)

The final keyword in java is used to restrict the user. The java final keyword can be used in many context. Final can be:

variable: If you make any variable as final, you cannot change the value of final variable(It will be constant).

method: If you make any method as final, you cannot override it.

class: If you make any class as final, you cannot extend it.

The final keyword can be applied with the variables, a final variable that have no value it is called blank final variable or uninitialized final variable. It can be initialized in the constructor only. The blank final variable can be static also which will be initialized in the static block only. We will have detailed learning of these. Let's first learn the basics of final keyword.



https://www.javatpoint.com/final-keyword#finalm
https://www.geeksforgeeks.org/final-keyword-in-java/


4.  What is Java garbage collection?

Garbage collection in Java is the process by which Java programs perform automatic memory management. Java programs compile to bytecode that can be run on a Java Virtual Machine, or JVM for short. When Java programs run on the JVM, objects are created on the heap, which is a portion of memory dedicated to the program. Eventually, some objects will no longer be needed. The garbage collector finds these unused objects and deletes them to free up memory.


https://www.geeksforgeeks.org/garbage-collection-java/

https://stackify.com/what-is-java-garbage-collection/#:~:text=Java%20garbage%20collection%20is%20the,memory%20dedicated%20to%20the%20program.

5.  What is the differences between super and this?

The this keyword points to a reference of the current class, while the super keyword points to a reference of the parent class. this can be used to access variables and methods of the current class, and super can be used to access variables and methods of the parent class from the subclass.

Since this and super keywords are related to an instance of an object, we cannot use them inside a static block or a static method. Failing to do so will result in compilation error non-static content this cannot be referenced from a static context.

https://www.techiedelight.com/difference-between-this-super-keyword-java/#:~:text=The%20this%20keyword%20points%20to,parent%20class%20from%20the%20subclass.

https://www.geeksforgeeks.org/difference-super-java/


6. Can we use this keyword in constructor and why?

Yes. Using this with a Constructor

From within a constructor, you can also use the this keyword to call another constructor in the same class. Doing so is called an explicit constructor invocation. Here's another Rectangle class, with a different implementation from the one in the Objects section.

```java
public class Rectangle {
    private int x, y;
    private int width, height;
        
    public Rectangle() {
        this(0, 0, 1, 1);
    }
    public Rectangle(int width, int height) {
        this(0, 0, width, height);
    }
    public Rectangle(int x, int y, int width, int height) {
        this.x = x;
        this.y = y;
        this.width = width;
        this.height = height;
    }
    ...
}
```
This class contains a set of constructors. Each constructor initializes some or all of the rectangle's member variables. The constructors provide a default value for any member variable whose initial value is not provided by an argument. For example, the no-argument constructor creates a 1x1 Rectangle at coordinates 0,0. The two-argument constructor calls the four-argument constructor, passing in the width and height but always using the 0,0 coordinates. As before, the compiler determines which constructor to call, based on the number and the type of arguments.

If present, the invocation of another constructor must be the first line in the constructor.

https://docs.oracle.com/javase/tutorial/java/javaOO/thiskey.html#:~:text=The%20most%20common%20reason%20for,a%20method%20or%20constructor%20parameter.&text=Each%20argument%20to%20the%20constructor,of%20the%20constructor's%20first%20argument


7. What is Runtime/unchecked exception? what is Compile/Checked Exception?

A checked exception is an exception that occurs at the compile time, these are also called as compile time exceptions. These exceptions cannot simply be ignored at the time of compilation, the programmer should take care of (handle) these exceptions.


An unchecked exception is an exception that occurs at the time of execution. These are also called as Runtime Exceptions. These include programming bugs, such as logic errors or improper use of an API. Runtime exceptions are ignored at the time of compilation.


https://www.tutorialspoint.com/Checked-vs-Unchecked-exceptions-in-Java#:~:text=An%20unchecked%20exception%20is%20an,at%20the%20time%20of%20compilation.




8. what is the difference between throw and throws?

Both throw and throws are concepts of exception handling in Java. The throws keyword is used to declare which exceptions can be thrown from a method, while the throw keyword is used to explicitly throw an exception within a method or block of code.

The throws keyword is used in a method signature and declares which exceptions can be thrown from a method. The throws keyword can be useful for propagating exceptions in the call stack and allows exceptions to not necessarily be handled within the method that declares these exceptions.

On the other hand, the throw keyword is used within a method body, or any block of code, and is used to explicitly throw a single exception. The throw keyword can be useful for throwing exceptions based on certain conditions within a code block and for throwing custom exceptions.


https://www.geeksforgeeks.org/difference-between-throw-and-throws-in-java/
https://www.tutorialspoint.com/difference-between-throw-and-throws-in-java
https://rollbar.com/blog/how-to-use-the-throws-keyword-in-java-and-when-to-use-throw/#:~:text=The%20throws%20keyword%20is%20used,method%20or%20block%20of%20code.

9. Run the below three pieces codes,Noticed the printed exceptions.  why do we put the Null/Runtime exception before Exception?

```java 
public class Main {
    public static void main(String[] args) {
        int a = 0;
        int b = 3
        String s = null;
        try {
            System.out.println(b / a);
            System.out.println(s.equals("aa"));
            throw new RuntimeException();
        } catch (ArithmeticException e) {
            e.printStackTrace();
        } catch (NullPointerException e) {
            e.printStackTrace();
        } catch (RuntimeException e) {
            e.printStackTrace();
        } catch (Exception e) {
            e.getMessage();
        }

        System.out.println("End ...");
    }
}

public class Main {
    public static void main(String[] args) {
        int a = 0;
        int b = 3
        String s = null;
        try {
            // System.out.println(b / a);
            System.out.println(s.equals("aa"));
            throw new RuntimeException();
        } catch (ArithmeticException e) {
            e.printStackTrace();
        } catch (NullPointerException e) {
            e.printStackTrace();
        } catch (RuntimeException e) {
            e.printStackTrace();
        } catch (Exception e) {
            e.getMessage();
        }

        System.out.println("End ...");
    }
}

public class Main {
    public static void main(String[] args) {
        int a = 0;
        int b = 3
        String s = null;
        try {
            // System.out.println(b / a);
            // System.out.println(s.equals("aa"));
            throw new RuntimeException();
        } catch (ArithmeticException e) {
            e.printStackTrace();
        } catch (NullPointerException e) {
            e.printStackTrace();
        } catch (RuntimeException e) {
            e.printStackTrace();
        } catch (Exception e) {
            e.getMessage();
        }

        System.out.println("End ...");
    }
}



``` 


