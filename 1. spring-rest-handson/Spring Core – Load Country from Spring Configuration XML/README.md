# Hands-on 4: Spring Core – Load Country from Spring Configuration XML

## Objective

This project demonstrates how to configure and load a Spring Bean using an XML configuration file. The application reads the Country bean from `country.xml` and displays its details using the Spring IoC Container.

## Technologies Used

- Java 21
- Spring Boot
- Spring Core
- Maven
- IntelliJ IDEA

## Project Structure

```
spring-learn
│── src
│   ├── main
│   │   ├── java
│   │   │   └── com.cognizant.springlearn
│   │   │       ├── SpringLearnApplication.java
│   │   │       └── Country.java
│   │   └── resources
│   │       ├── application.properties
│   │       └── country.xml
│── pom.xml
```

## Features

- Configures a Spring Bean using XML.
- Loads the bean using `ClassPathXmlApplicationContext`.
- Demonstrates Spring IoC (Inversion of Control).
- Displays Country details from the XML configuration.
- Includes constructor and setter invocation logs.

## XML Configuration

The `country.xml` file defines a Spring bean named `country` with the following properties:

- Code : IN
- Name : India

## How to Run

1. Clone the repository.
2. Open the project in IntelliJ IDEA.
3. Update Maven dependencies.
4. Run the `SpringLearnApplication.java` file.
5. Observe the console output.

## Expected Output

```
Inside Country Constructor.
Inside setCode()
Inside setName()
Country [code=IN, name=India]
```

## Concepts Covered

- Spring Core
- Spring IoC Container
- Bean Configuration using XML
- Dependency Injection using Setter Injection
- ApplicationContext
- ClassPathXmlApplicationContext
- Maven Project Structure

## Author

Neha Sankeerthana
