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
