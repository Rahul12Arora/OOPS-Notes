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


<h2>Static Vs Final Variables</h2>

In Java, both static and final are keywords used to declare variables with specific properties.</br>

A static variable is a class-level variable, which means that its value is shared across all instances of that class. It can be accessed without creating an instance of the class. When a variable is declared as static, it belongs to the class and not to any specific object of that class.</br>

On the other hand, a final variable is a constant variable whose value cannot be changed once it is initialized. A final variable can be initialized in the following ways:</br>

<ul>
Directly during declaration
  <li>In the constructor of the class</li>
  <li>In an instance initialization block</li>
  <li>In a static initialization block</li>
</ul>

A final variable can be declared as either an instance variable or a class variable (static final). When a final variable is declared as an instance variable, it means that each instance of the class will have its own copy of the variable, and once it is initialized, its value cannot be changed. When a final variable is declared as a class variable (static final), it means that the variable is a constant that is shared across all instances of the class.</br>

In summary, static variables are class-level variables that can be accessed without creating an instance of the class, while final variables are constant variables whose value cannot be changed once it is initialized.</br>
