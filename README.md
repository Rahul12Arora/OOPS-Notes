# OOPS-Notes

<h2>Object</h2>

**An object is an instance of a class. It is a runtime entity that contains its own set of attributes (data members) and methods (functions) as defined in the class.**</br>
An Object is a real-world element in an object-oriented environment that may have physical or conceptual existence.

</br>

<h2>Class</h2>

**A class is a blueprint or a template for creating objects, which defines a set of attributes (data members) and methods (functions) that the objects of that class will have.**</br>

NOT REAL: Class is not a REAL THING; it’s just a concept, actually the objects created from a class are real.
</br>
A single class can be used to create any number of instances or objects.
</br>

<h2>Procedural vs Object Oriented Paradigm</h2>
<ol>

<li>Both paradigms are used to write computer programs, but they have different approaches to organizing and manipulating data and behavior.</li>

<li>Procedural programming focuses on procedures and functions, while object-oriented design focuses on objects and classes.</li>

<li>In procedural programming, data and behavior are typically separated into different parts of the program, with data stored in variables or data structures and behavior implemented as functions or procedures that manipulate that data. In contrast, in object-oriented design, data and behavior are encapsulated together within objects, with objects representing a self-contained unit that combines data and behavior in a single entity. This makes it easier to manage the complexity of the program, and helps to ensure that data is used and manipulated in a consistent and safe manner.</li>

<li>Both paradigms promote code reusability, but object-oriented design does so through inheritance and polymorphism, while procedural programming relies on functions that can be reused in different parts of the program.</li>

<li>Object-oriented design promotes modularity by allowing objects to be developed independently and combined as needed, while procedural programming often relies on larger functions that contain multiple steps.</li>

<li>Encapsulation is a key concept in object-oriented design, which protects an object's internal state from outside interference. In procedural programming, data is often shared across functions, which can lead to unexpected changes in program state.</li>

<li>In terms of code organization style, procedural programming typically uses a top-down approach, while object-oriented design uses a bottom-up approach.</li>

<li>Examples of procedural programming languages include C, Pascal, and Fortran, while examples of object-oriented programming languages include Java, C++, Python, and Ruby.</li>

</ol>

<h2>Software Development Process</h2>

![image](https://user-images.githubusercontent.com/108695777/231948701-0a233105-dccd-4369-a746-d75e75e479c5.png)


<h2>UML</h2>
**The Unified Modeling Language (UML) is a standard graphical language for modeling object-oriented software.**

<h3>UML Diagrams</h3>
As UML is a graphical language, it supports two types of diagrams that can be classified as Structural and Behavioral.</br>

The structural Diagrams are used to create a static model of the software. That is, it gives an idea about what all components build up the system.</br>

The Behavioral Diagrams are used to create a dynamic model of the software. It tells how the different components or modules interact with each other.</br>

![image](https://user-images.githubusercontent.com/108695777/232028973-f2ecaf75-dc11-4ffb-ad0f-c822fd3ca9f9.png)


Some of the structural and behavioral diagrams supported by UML are as shown:</br>
![image](https://user-images.githubusercontent.com/108695777/231949305-d14c546f-21bb-4894-b0c5-da92703483cd.png)

<h3>Class Diagrams in UML</h3>
A Class/Class diagram in UML Consists of 3 parts
<ul>
  <li>Class Name</li>
  <li>Class Properties</li>
  <li>Class Methods</li>
</ul>
**A class diagram in the Unified Modeling Language (UML) is a type of structural diagram that describes the structure of a system by showing the System's Classes, their Attributes, Operations (or methods), and the relationships among objects.**</br>


<h1>Generalization</h1>

**Generalization is a key concept in object-oriented programming, and it refers to the process of creating a more general (or abstract) superclass that defines common attributes and behaviors for a group of related subclasses.**


<h2>Abstract Classes & Interfaces</h2>

![image](https://user-images.githubusercontent.com/108695777/232040280-03c2016c-46f5-40df-b99d-c393acc6b7de.png)

```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Vehicle v = new Car(4,1,5,100);     //LHS dictates what are the reference methods available, RHS actually implements those methods
        v.display();        //Allowed => now both Vehicle & Car have display method(), but Car over-rides Vehicle; down to up approach.
        // v.carOnlyMethod();  //Not Allowed => because only reference methods of the Vehicle class are available.

        Iterable<Integer> iarr = new ArrayList<>();   // only methods(11) of Iterable are present with iarr, ArrayList implements them
        Collection<Integer> carr = new ArrayList<>(); // all methods(20) of Colection are present with carr, ArrayList implements them
        List<Integer> larr = new ArrayList<>();       // all methods(30) of List are present with larr, ArrayList implements them
        ArrayList<Integer> arr = new ArrayList<>();   // all methods(30) of ArrayList are present with iarr, ArrayList implements them


    }
    static class Vehicle{
        int wheels;
        int power;
        public Vehicle(int wheels, int power){
            this.wheels=wheels;
            this.power=power;
        }

        public void display(){
            System.out.println("Hello i am vehicle's method with data");
        }

    }
    static class Car extends Vehicle{
    int doors;
    int handle;
    public Car(int doors, int handle, int wheels, int power){
        super(wheels,power);
        this.doors=doors;
        this.handle=handle;
    }
        public void display(){
            System.out.println("Hello i am car's method with data");
        }
        public void carOnlyMethod(){
            System.out.println("Hello i am car's method with data");
        }

    }

}

//Static variable is only accessible in static method
//In a java file only a single public Main class with a static main method must exist, all other classes cannot be public/static
```

<h1>Super Keyword</h1>
In Java, the super keyword is used to refer to the parent class of a subclass, while this represents to the current class.

<ol>
<li>super is used to call a superclass constructor: When a subclass is created, its constructor must call the constructor of its parent class. This is done using the <li>super() keyword, which calls the constructor of the parent class.</li>
<li>super is used to call a superclass method: A subclass can call a method defined in its parent class using the super keyword. This is useful when the subclass wants to invoke the parent class’s implementation of the method in addition to its own.</li>
<li>super is used to access a superclass field: A subclass can access a field defined in its parent class using the super keyword. This is useful when the subclass wants to reference the parent class’s version of a field.</li>
<li>super must be the first statement in a constructor: When calling a superclass constructor, the super() statement must be the first statement in the constructor of the subclass.</li>
<li>super cannot be used in a static context: The super keyword cannot be used in a static context, such as in a static method or a static variable initializer.</li>
<li>super is not required to call a superclass method: While it is possible to use the super keyword to call a method in the parent class, it is not required. If a method is not overridden in the subclass, then calling it without the super keyword will invoke the parent class’s implementation.</li>
</ol>


<ul>
<li>Call to super() must be the first statement in the Derived(Student) Class constructor because if you think about it, it makes sense that the superclass has no knowledge of any subclass, so any initialization it needs to perform is separate from and possibly prerequisite to any initialization performed by the subclass. Therefore, it needs to complete its execution first.</li>
<li>If a constructor does not explicitly invoke a superclass constructor, the Java compiler automatically inserts a call to the no-argument constructor of the superclass. If the superclass does not have a no-argument constructor, you will get a compile-time error. The object does have such a constructor, so if the Object is the only superclass, there is no problem.</li>
  
![image](https://user-images.githubusercontent.com/108695777/232190859-94ce250d-e83d-4cae-8897-e890bc458299.png)

<li>If a subclass constructor invokes a constructor of its superclass, either explicitly or implicitly, you might think that a whole chain of constructors is called, all the way back to the constructor of Object. This, in fact, is the case. It is called constructor chaining.</li>
</ul>







<h1>Static</h1>

<h2>Static Vs Final Variables</h2>

In Java, both static and final are keywords used to declare variables with specific properties.</br>

**A static variable is a class-level variable, which means that its value is shared across all instances of that class. It can be accessed without creating an instance of the class. When a variable is declared as static, it belongs to the class(even non-static classes) and not to any specific object of that class.**</br>

**Static variable in Java is variable which belongs to the class and initialized only once at the start of the execution.**

** Static variables are initialized only once, at the start of the execution. These variables will be initialized first, before the initialization of any instance variables**

On the other hand, a final variable is a constant variable whose value cannot be changed once it is initialized. A final variable can be initialized in the following ways:</br>

<ul>
Directly during declaration
  <li>In the constructor of the class</li>
  <li>In an instance initialization block</li>
  <li>In a static initialization block</li>
</ul>

A final variable can be declared as either an instance variable or a class variable (static final). When a final variable is declared as an instance variable, it means that each instance of the class will have its own copy of the variable, and once it is initialized, its value cannot be changed. When a final variable is declared as a class variable (static final), it means that the variable is a constant that is shared across all instances of the class.</br>

In summary, static variables are class-level variables that can be accessed without creating an instance of the class, while final variables are constant variables whose value cannot be changed once it is initialized.</br>

<h2>Static class in Java</h2>
<ul>
<li>In java, we have static instance variables as well as static methods and also static block. Classes can also be made static in Java.</li>

<li>Java allows us to define a class within another class. Such a class is called a nested class. The class which enclosed nested class is known as Outer class. In java, we can’t make Top level class static. Only nested classes can be static.</li>
  
</ul>

```
/* Java program to demonstrate how to implement static and non-static
classes in a java program. */
class OuterClass{
    private static String msg = "CECS 277";
    // Static nested class
    public static class NestedStaticClass{
        // Only static members of Outer class is directly accessible in nested
// static class
        public void printMessage() {
// Try making 'message' a non-static variable, there will be
// compiler error
            System.out.println("Message from nested static class: " + msg);
        }
    }
    // non-static nested class - also called Inner class
    public class InnerClass{
// Both static and non-static members of Outer class are accessible in
// this Inner class
        public void display(){
            System.out.println("Message from non-static nested class: "+ msg);
        }
    }
}
class Main
{
    // How to create instance of static and non static nested class?
    public static void main(String args[]){
// create instance of nested Static class
        OuterClass.NestedStaticClass printer = new OuterClass.NestedStaticClass();
// call non static method of nested static class
        printer.printMessage();
// In order to create instance of Inner class we need an Outer class
// instance. Let us create Outer class instance for creating
// non-static nested class
        OuterClass outer = new OuterClass();
        OuterClass.InnerClass inner = outer.new InnerClass();
// calling non-static method of Inner class
        inner.display();
// we can also combine above steps in one step to create instance of
// Inner class
        OuterClass.InnerClass innerObject = new OuterClass().new InnerClass();
// similarly we can now call Inner class method
        innerObject.display();
    }
}
```

<h2>Static Methods</h2>

***What is Static Method in Java?***

Static method in Java is a method which belongs to the class and not to the object, A static method can access only static data.</br>
<ol>
<li> It is a method which belongs to the class and not to the object(instance)</li>
<li> A static method can access only static data. It can not access non-static data(instance variables)</li>
<li> A static method can call only other static methods and can not call a nonstatic method from it.</li>
<li> A static method can be accessed directly by the class name and doesn’t need any object</li>
<li> A static method cannot refer to "this" or "super" keywords in anyway.</li>
</ol>
Syntax : <class-name>.<method-name></br>
Note: main method is static, since it must be accessible for an application to run, before any instantiation takes place.
