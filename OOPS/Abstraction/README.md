## Abstraction

- Abstraction is the process of hiding the internal details of an application from the outer world.
- Abstraction is used to describe things in simple terms.
- It’s used to create a boundary between the application and the client programs.
<br/>

- Abstraction in Java is the process in which we only show essential details/functionality to the user. The non-essential implementation details are not displayed to the user.
<br/>


- **Abstraction in Real life**
    - Your car is a great example of abstraction. You can start a car by turning the key or pressing the start button. You don’t need to know how the engine is getting 
      started, what all components your car has. The car internal implementation and complex logic is completely hidden from the user.
    - We can heat our food in Microwave. We press some buttons to set the timer and type of food. Finally, we get a hot and delicious meal. The microwave internal details are 
      hidden from us. We have been given access to the functionality in a very simple manner.
<br/>

- Abstraction in Java is implemented through **interfaces** and **abstract classes**. They are used to create a base implementation or contract for the actual implementation classes.

### Abstract Class

- In Java, an abstract class is a class that cannot be instantiated on its own and typically serves as a blueprint for other classes.
- Declared using the _abstract_ keyword.
- Can contain abstract methods (methods without a body) as well as concrete methods (methods with a body).
- _Abstract classes are used when you want to provide a common interface for a group of related classes, but you want to leave some methods to be implemented by the subclasses._
- An **abstract method** is a method declared without an implementation. It’s used to define the signature of a method that must be implemented by non-abstract subclasses. Abstract methods are declared using the _abstract_ keyword and do not contain a method body. Any class containing one or more abstract methods must be declared as abstract.
- _extends_ is the keyword used in the subclass to extend a abstract class

### Interface

- An interface is similar to an abstract class in that it cannot be instantiated, but it differs in its purpose.
- An interface provides a contract for its implementers to follow, specifying a set of methods that must be implemented.
- In Java, interfaces are declared using the _interface_ keyword.

Example that shows both abstract class and interface
---------------------------------------------------

![alt text](https://github.com/akin-a/notes/blob/main/images/OOPS/Abstraction.png)
