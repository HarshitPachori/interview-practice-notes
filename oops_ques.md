#### Q1. What is OOP?

Object-Oriented Programming (OOP) is a programming paradigm that organizes software design around "objects" that encapsulate data (attributes) and related behavior (methods). Objects interact with each other through method calls.

#### Q2. Explain the difference between Procedural Programming and OOP.

- `Procedural Programming`: Focuses on breaking down programs into functions or procedures that perform specific tasks. Data is often global or shared between functions.
- `OOP`: Decomposes programs into objects, promoting data hiding and modularity.

#### Q3. Real-World Example:

- `Procedural`: Imagine a recipe as a set of instructions (functions) to prepare a dish. Ingredients (data) could be passed between functions.
- `OOP`: In OOP, the recipe itself would be an object with properties like ingredients and methods for preparation steps. Each dish instance could be a separate object.

#### Q4. What are the four pillars of OOP?

- `Encapsulation`: Bundling data (attributes) and related methods that operate on that data within a single unit (class).
- `Inheritance`: Deriving new classes (subclasses) from existing ones (parent classes) to reuse code and extend functionality.
- `Polymorphism`: The ability of objects to respond differently to the same method call based on their type.
- `Abstraction`: Exposing essential details while hiding implementation specifics, providing a simplified interface for users.

#### Q5. Explain the concept of a class and an object in Java.

- `Class`: A blueprint or template that defines the properties (attributes) and methods (functions) that objects of that class will share.
- `Object`: An instance of a class, representing a specific entity with its own set of attributes and methods.

#### Q6. Real-World Example:

- `Class`: A class named Car could define attributes like color, model, engine, and methods like startEngine, accelerate, and brake.
- `Object`: A specific car (e.g., a red Honda Civic) would be an object of the Car class with its own values for attributes and the ability to use the defined methods.

#### Q7. What is a constructor in Java?

A special method with the same name as the class that is invoked when an object is created. It's used to initialize the object's attributes.

#### Q8. What is the keyword this used for?

Inside a class method, the this keyword refers to the current object instance. It's used to access the object's attributes and methods within the method.

#### Q9. Explain Inheritance with a real-world example.

Inheritance allows a subclass (child class) to inherit attributes and methods from a parent class. The subclass can add its own specific attributes and methods or override inherited methods to provide specialized behavior.

- Real-World Example:

  - A parent class Animal could have attributes like name and age and methods like eat and sleep.
  - Subclasses like Dog and Cat could inherit these properties and add specific methods like bark and meow, respectively.

#### Q10. What are the different types of inheritance in Java?

- `Single Inheritance`: A class inherits from one parent class.
- `Multilevel Inheritance`: A class inherits from another class that itself inherits from a parent class (creating a hierarchy).
- `Hierarchical Inheritance`: Multiple subclasses inherit from a single parent class.
- `Interface Inheritance`: Interfaces can inherit from other interfaces, extending their functionalities.

#### Q11. Explain the difference between abstract and final classes.

- `Abstract Class`: A class that cannot be instantiated directly (cannot create objects) but serves as a blueprint for subclasses to inherit from. Often defines abstract methods (methods without implementation) that subclasses must implement.
- `Final Class:` A class that cannot be subclassed (inherited from) to prevent further specialization.

#### Q12. What is Polymorphism in Java? Explain its types.

Polymorphism allows objects of different classes to respond differently to the same method call at runtime.

Types of Polymorphism:

- `Compile-Time Polymorphism (Method Overloading)`: Multiple methods within a class have the same name but different parameter lists. The compiler determines the correct method based on argument types.

- `Runtime Polymorphism (Method Overriding)`: Subclasses can override methods inherited from a parent class to provide their own implementation.

Real-World Example:

A parent class Shape could have an abstract method area() to calculate area (specific implementation depends on the shape).
Subclasses like Circle and Square would override area() with their own formulas. Calling area() on a Circle object would execute the circle's specific implementation.

#### Q13. What are interfaces in Java?

Interfaces are blueprints that define a set of methods (without implementation) that classes can implement. They promote loose coupling (focus on what a class can do, not how it does it).

Real-World Example:

- An interface Drawable could define a method draw().
- Classes like Circle and Square could implement Drawable and provide their own implementations for draw(), specifying how to draw the respective shapes.

#### Q14. Explain the concept of packages in Java.

Packages organize related classes and interfaces into a hierarchical structure to promote code maintainability, reusability, and avoid naming conflicts.

Real-World Example:

- A package com.example.shapes could contain classes like Circle, Square, and Shape (interface).
- Another package com.example.animals could contain classes like Dog and Cat.

#### Q15. Explain the concept of Exception Handling in Java.

Exception handling is a mechanism to manage errors and exceptions that occur during program execution. It allows you to define custom behavior for different types of exceptions, preventing program crashes.

Java uses try...catch blocks for exception handling:

```Java
try {
  // Code that might throw an exception
} catch (ExceptionType1 e) {
  // Handle ExceptionType1
} catch (ExceptionType2 e) {
  // Handle ExceptionType2
} finally {
  // Code that always executes, regardless of exceptions
}
```

#### Q16. What is the difference between checked and unchecked exceptions?

- `Checked Exceptions:` Inherited from the Exception class, they must be declared or handled using try...catch blocks. Examples include IOException and FileNotFoundException.

- `Unchecked Exceptions:` Inherited from the RuntimeException class, they don't require explicit declaration or handling but can still disrupt program flow. Examples include NullPointerException and IndexOutOfBoundsException.

#### Q17. Explain Inner Classes in Java.

Inner classes are classes defined within another class. They can access the enclosing class's members directly and provide a way to create classes that are tightly coupled to the outer class.

Types of Inner Classes:

- `Member Inner Classes`: Defined within a class but outside of any method.
- `Static Inner Classes: `Defined within a class and declared as static. They cannot access non-static members of the enclosing class.
- `Local Inner Classes:` Defined within a method and have access to the local variables of that method.
- `Anonymous Inner Classes:` Defined and instantiated without a separate class name. Often used for short, one-time use implementations of interfaces. 16. Explain Abstract Classes and Interfaces in detail.

#### Q18. Abstract Classes: (Already covered in Intermediate Concepts)

- Cannot be directly instantiated.
- Can define abstract methods (without implementation) that subclasses must implement.
- Can have concrete methods as well.
- Used to enforce common behavior and structure for subclasses.

#### Q19. Interfaces: (Already covered in Intermediate Concepts)

- Define contracts (method signatures) without implementation.
- Classes can implement multiple interfaces.
- Promote loose coupling and code reusability. 17.

#### Q20. Explain the difference between abstract and interface in Java.

- `Abstract classes`: Can have concrete methods and state (attributes).

- `Interfaces:` Only define method signatures; no implementation or state.

#### Q21. Explain the concept of Design Patterns in OOP.

Design patterns are reusable solutions to common software design problems. They provide a high-level blueprint for structuring code to promote maintainability, flexibility, and reusability.

Examples of Design Patterns:

- `Singleton Pattern:` Ensures only one instance of a class exists.
- ` Factory Pattern`: Creates objects without exposing creation logic.
- `Observer Pattern`: Defines a one-to-many dependency between objects, where changes to one object (subject) notify dependent objects (observers)
- `Adapter Pattern`: Allows incompatible interfaces to work together.
- `Strategy Pattern`: Allows changing an object's behavior at runtime.

#### Q22. Explain how access modifiers (public, private, protected) are used in Java.

Access modifiers control the visibility and accessibility of classes, attributes, and methods within a class or package.

- `public`: Members are accessible from anywhere in the program.

- `private`: Members are only accessible within the class they are defined.

- `protected`: Members are accessible within the class they are defined, its subclasses within the same package, and classes in other packages given explicit permission.

#### Q23. Explain the benefits of using OOP principles in Java.

- `Modularization`: Breaks down complex problems into smaller, manageable units (objects).
- `Encapsulation`: Data hiding promotes security and reduces the risk of unintended modifications.
- `Reusability`: Code can be reused through inheritance and interfaces.
- `Maintainability`: Easier to understand, modify, and extend code due to modular structure.
- `Flexibility`: Objects can be easily adapted to different scenarios.

