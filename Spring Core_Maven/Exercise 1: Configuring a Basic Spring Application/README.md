# Exercise 1 – Configuring a Basic Spring Application

## Objective

The objective of this exercise is to understand the fundamentals of the **Spring Framework** by configuring a basic Spring application using **XML-based bean configuration**. This exercise demonstrates how Spring manages objects (beans) and performs Dependency Injection (DI).

---

## Scenario

A company is developing a **Library Management System**. The backend is built using the Spring Framework to manage application components efficiently. The application consists of a service layer (`BookService`) and a repository layer (`BookRepository`), which are configured and managed using the Spring IoC Container.

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

Add the Spring Context dependency to `pom.xml`.

```xml
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-context</artifactId>
    <version>5.3.39</version>
</dependency>
```

---

## Files Description

### BookRepository.java

Represents the repository layer responsible for data access operations.

```java
public void displayRepository() {
    System.out.println("Book Repository Created");
}
```

---

### BookService.java

Represents the service layer. It depends on `BookRepository` and receives it through Spring Dependency Injection.

```java
public void displayService() {
    System.out.println("Book Service Created");
    repository.displayRepository();
}
```

---

### applicationContext.xml

Defines Spring beans and configures Dependency Injection.

```xml
<bean id="bookRepository"
      class="com.library.repository.BookRepository"/>

<bean id="bookService"
      class="com.library.service.BookService">

    <property name="repository"
              ref="bookRepository"/>

</bean>
```

---

### Main.java

Loads the Spring Application Context, retrieves the `BookService` bean, and invokes its method.

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
4. Spring injects `BookRepository` into `BookService`.
5. The application retrieves the `BookService` bean.
6. The `displayService()` method is executed.
7. The repository method is invoked.

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
- Bean Configuration
- XML-based Configuration
- Maven Dependency Management
- Application Context
- Bean Creation and Management

---

## Learning Outcomes

- Understand the architecture of a basic Spring application.
- Configure Spring beans using XML.
- Implement Dependency Injection using setter injection.
- Load and use the Spring Application Context.
- Understand how the Spring IoC Container manages application components.

---

## Conclusion

This exercise demonstrates the fundamentals of the Spring Framework by configuring beans using an XML configuration file. It shows how Spring's IoC Container creates, manages, and injects dependencies, resulting in a loosely coupled and maintainable application.
