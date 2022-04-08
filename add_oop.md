1. Type of methods: Interface can have only abstract methods. An abstract class can have abstract and non-abstract methods. From Java 8, it can have 
default and static methods also. Final Variables: Variables declared in a Java interface are by default final. An abstract class may contain non-final 
variables. Type of variables: Abstract class can have final, non-final, static and non-static variables. The interface has only static and final 
variables. Implementation: Abstract class can provide the implementation of the interface. Interface can’t provide the implementation of an 
abstract class. Inheritance vs Abstraction: A Java interface can be implemented using the keyword “implements” and an abstract class can be extended 
using the keyword “extends”. Multiple implementations: An interface can extend another Java interface only, an abstract class can extend another 
Java class and implement multiple Java interfaces. Accessibility of Data Members: Members of a Java interface are public by default. A Java abstract
class can have class members like private, protected, etc.```
2.Overriding implements Runtime Polymorphism whereas Overloading implements Compile time polymorphism.
The method Overriding occurs between superclass and subclass. Overloading occurs between the methods in the same class.
Overriding methods have the same signature i.e. same name and method arguments. Overloaded method names are the same but the parameters are different.
With Overloading, the method to call is determined at the compile-time. With overriding, the method call is determined at the runtime based on 
the object type.
If overriding breaks, it can cause serious issues in our program because the effect will be visible at runtime. Whereas if overloading breaks, 
the compile-time error will come and it’s easy to fix.
3. final method ---prevent method overriding
   final class ----prevent inheritance
   final varible-----make it as a constant varible
4.ava programs compile to bytecode that can be run on a Java Virtual Machine, or JVM for short. When Java programs run on the JVM, objects are created on
the heap, which is a portion of memory dedicated to the program. Eventually, some objects will no longer be needed. The garbage collector finds these 
unused objects and deletes them to free up memory.
5. super keyword is used to access methods of the parent class while this is used to access methods of the current class.
6.A constructor in Java is a special method that is used to initialize objects. The constructor is called when an object of a class is created. 
It can be used to set initial values for object attributes. 
7. RuntimeException --- This represents any exception which occurs during runtime.
8.throws is a keyword in Java which is used in the signature of method to indicate that this method might throw one of the listed type exceptions. 
The caller to these methods has to handle the exception using a try-catch block. 
9. 
output1: java.lang.ArithmeticException: / by zero
	at Main.main(Main.java:7)
output2: 
