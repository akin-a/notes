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
