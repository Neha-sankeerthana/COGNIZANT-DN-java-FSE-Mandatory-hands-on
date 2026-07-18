# Exercise 2 – Implementing Dependency Injection

## Objective

The objective of this exercise is to understand **Dependency Injection (DI)** using the **Spring Framework**. This exercise demonstrates how Spring's **Inversion of Control (IoC) Container** manages dependencies between application components through **setter-based dependency injection**.

---

## Scenario

In the **Library Management System**, the `BookService` class depends on the `BookRepository` class to perform repository operations. Instead of manually creating objects, Spring manages and injects the required dependency using XML configuration.

---

## Technologies Used

- Java
- Spring Framework (Spring Core)
- Maven
- IntelliJ IDEA

---

## Project Structure

```
LibraryManagement
│
├── pom.xml
│
└── src
    ├── main
    │   ├── java
    │   │   └── com.library
    │   │       ├── Main.java
    │   │       ├── repository
    │   │       │   └── BookRepository.java
    │   │       └── service
    │   │           └── BookService.java
    │   │
    │   └── resources
    │       └── applicationContext.xml
    │
    └── test
```

---

## Maven Dependency

```xml
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-context</artifactId>
    <version>5.3.39</version>
</dependency>
```

---

## Implementation

### BookRepository.java

Represents the repository layer.

```java
public class BookRepository {

    public void displayRepository() {
        System.out.println("Book Repository Created");
    }

}
```

---

### BookService.java

Implements setter-based dependency injection.

```java
private BookRepository bookRepository;

public void setBookRepository(BookRepository bookRepository) {
    this.bookRepository = bookRepository;
}

public void displayService() {
    System.out.println("Book Service Created");
    bookRepository.displayRepository();
}
```

---

### applicationContext.xml

Configures Spring beans and injects the dependency.

```xml
<bean id="bookRepository"
      class="com.library.repository.BookRepository"/>

<bean id="bookService"
      class="com.library.service.BookService">

    <property name="bookRepository"
              ref="bookRepository"/>

</bean>
```

---

### Main.java

Loads the Spring Application Context and retrieves the `BookService` bean.

```java
ApplicationContext context =
        new ClassPathXmlApplicationContext("applicationContext.xml");

BookService service =
        context.getBean("bookService", BookService.class);

service.displayService();
```

---

## Program Flow

1. Load the Spring Application Context.
2. Spring creates the `BookRepository` bean.
3. Spring creates the `BookService` bean.
4. Spring injects the `BookRepository` bean into `BookService` using setter injection.
5. The `displayService()` method is invoked.
6. `BookService` calls `BookRepository`.

---

## Expected Output

```
Book Service Created
Book Repository Created
```

---

## Spring Concepts Covered

- Spring Framework
- Spring IoC (Inversion of Control)
- Dependency Injection (DI)
- Setter Injection
- Bean Configuration
- XML Configuration
- Application Context
- Bean Wiring

---

## Learning Outcomes

- Understand the concept of Dependency Injection.
- Configure dependencies using XML-based Spring configuration.
- Implement setter injection in Spring.
- Learn how Spring IoC Container manages object creation and dependency wiring.
- Develop loosely coupled and maintainable applications using Spring.

---

## Conclusion

This exercise demonstrates how Spring's IoC Container automatically injects dependencies between application components using **setter-based dependency injection**. By managing object creation and wiring through XML configuration, Spring promotes loose coupling, better maintainability, and improved code reusability.
