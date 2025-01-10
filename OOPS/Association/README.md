## Association

- Association is the OOPS concept to define the relationship between objects.
- It represents a general “has-a” or “uses-a” relationship between objects, allowing them to communicate.
- Association can be unidirectional (one-way) or bidirectional (two-way), depending on whether the relationship is defined in one or both classes.
- There can be four types of association between the objects:
   - One to One
   - One to Many
   - Many to One, and
   - Many to Many
- **Practical example** : Let's understand the relationship with real-time examples. For example, a country can have one prime minister (one to one), and a prime minister can have many ministers (one to many). Also, many MP's can have one prime minister (many to one), and many ministers can have many departments (many to many).

Example
Consider a library system with Author and Book classes:

```
public class Author {
    private String name;
    public Author(String name) {
        this.name = name;
    }
    // Getters and setters
}
public class Book {
    private String title;
    private Author author;
    public Book(String title, Author author) {
        this.title = title;
        this.author = author;
    }
    // Getters and setters
}
```
In this example, a Book has an Author object, representing a unidirectional association relationship. The Book class has a reference to the Author class, indicating that a book has an author. However, the Author class does not have any reference to the Book class, so the relationship is one-way.

If we want to make the relationship bidirectional, we can modify the Author class to include a list of Book objects:

### Aggregation

- Aggregation is a way to achieve Association.
- Aggregation represents the relationship where one object contains other objects as a part of its state.
- It represents the **weak** relationship between objects.
- It is also termed as a **has-a** relationship in Java.
- In aggregation, the composed object (whole) can exist independently of its parts, and the whole does not manage the lifetime of the parts. If the whole is destroyed, the parts can still exist.
<br/>

Example,
Consider a university system with Department and Professor classes:

```
public class Professor {
    private String name;
    public Professor(String name) {
        this.name = name;
    }
    // Getters and setters
}
public class Department {
    private String name;
    private List<Professor> professors;
    public Department(String name) {
        this.name = name;
        this.professors = new ArrayList<>();
    }
    public void addProfessor(Professor professor) {
        professors.add(professor);
    }
    // Getters and setters
}
```

In this example, a Department has a list of Professor objects, representing an aggregation relationship. The Department and Professor objects can exist independently of each other. If a Department is destroyed, the Professor objects can still exist and be associated with other departments.

### Composition

- The composition is also a way to achieve Association.
- The composition represents the relationship where one object contains other objects as a part of its state.
- There is a **strong** relationship between the containing object and the dependent object.
- It is the state where containing objects do not have an independent existence.
- If we delete the parent object, all the child objects will be deleted automatically.
- A composition is an intense form of association that represents a “has-a” or “part-of” relationship between objects, similar to aggregation. However, in composition, the composed object (entire) is responsible for managing the lifetime of its parts. If the entire is destroyed, its parts are also destroyed.

<br/>
**Example**

Consider a computer system with Computer and Processor classes:

```
public class Processor {
    private String model;
    public Processor(String model) {
        this.model = model;
    }
    // Getters and setters
}
public class Computer {
    private String name;
    private Processor processor;
    public Computer(String name, String processorModel) {
        this.name = name;
        this.processor = new Processor(processorModel);
    }
    // Getters and setters
```
In this example, a Computer has a Processor object, representing a composition relationship. The Computer object is responsible for creating and managing the lifetime of its Processor. If a Computer is destroyed, its Processor object is also destroyed, as it cannot exist independently.


