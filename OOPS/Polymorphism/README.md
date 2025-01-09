## Polymorphism

- Polymorphism is the concept where an object behaves differently in different situations.
- The ability of an object to take on different forms.
- A nice read on Polymorphism is [here](https://medium.com/@AlexanderObregon/beginners-guide-to-java-polymorphism-a35ee0d67e35)

### Compile time polymorphism - Method overloading

- Same method name, different arguments

### Rum time polymorphism - Method overriding

- Method in the child class has the same name, return-type and parameters as in parent class
- Unlike overloading, where methods are differentiated by their signatures, overriding involves a subclass providing a specific implementation for a method that is already defined in its superclass.
- The decision about which method implementation to execute is deferred until runtime, based on the object’s actual type.
- _Practical use:_ It gets useful when you have different types of objects and can write classes that can work with all those different types because they all adhere to the same API. Like below example, u can create muliple objects of type Vehicle eventhough each refers to different class.
- Eventhough all the method names are same, compiler wouldnt know which method is to be invoked (as both parent and subclass has the method) rather it will be invoked dynamically during the runtime based on which object is created.

![alt text](https://github.com/akin-a/notes/blob/main/images/OOPS/Polymorphism.png)

