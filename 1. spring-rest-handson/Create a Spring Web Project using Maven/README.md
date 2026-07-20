# Spring REST - Hands-on 1
## Create a Spring Web Project using Maven

### Objective
The objective of this hands-on is to create a Spring Boot web application using Maven, understand the project structure, configure dependencies, and successfully run the application using the embedded Tomcat server.

---

## Project Information

- **Project Name:** spring-learn
- **Group ID:** com.cognizant
- **Artifact ID:** spring-learn
- **Language:** Java
- **Build Tool:** Maven
- **Java Version:** 21
- **Spring Boot Version:** 4.1.0

---

## Technologies Used

- Java 21
- Spring Boot
- Spring Web MVC
- Maven
- Spring Boot DevTools
- Embedded Apache Tomcat
- IntelliJ IDEA

---

## Project Structure

```
spring-learn
│
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com.cognizant.springlearn
│   │   │       └── SpringLearnApplication.java
│   │   └── resources
│   │       ├── application.properties
│   │       ├── static
│   │       └── templates
│   │
│   └── test
│       └── java
│
├── pom.xml
└── README.md
```

---

## Dependencies

The project uses the following dependencies:

- Spring Boot Starter Web MVC
- Spring Boot DevTools
- Spring Boot Starter Web MVC Test

These dependencies provide:

- Spring MVC framework
- Embedded Apache Tomcat Server
- JSON support using Jackson
- Development tools with automatic restart
- Testing support

---

## Main Class

```
SpringLearnApplication.java
```

This is the entry point of the application.

```java
@SpringBootApplication
public class SpringLearnApplication {

    public static void main(String[] args) {
        SpringApplication.run(SpringLearnApplication.class, args);
    }

}
```

---

## @SpringBootApplication

The `@SpringBootApplication` annotation combines:

- `@Configuration`
- `@EnableAutoConfiguration`
- `@ComponentScan`

It enables auto-configuration, component scanning, and configuration support for the Spring Boot application.

---

## How to Run

1. Open the project in IntelliJ IDEA.
2. Open `SpringLearnApplication.java`.
3. Click the **Run** button or right-click and select **Run 'SpringLearnApplication'**.
4. Wait until the application starts successfully.

---

## Expected Output

```
Starting SpringLearnApplication

Tomcat started on port 8080 (http)

Started SpringLearnApplication
```

The application starts successfully using the embedded Tomcat server on **http://localhost:8080**.

---

## Maven Dependency Hierarchy

The project dependency tree includes:

- spring-boot-starter-webmvc
- spring-boot-devtools
- spring-boot-starter-webmvc-test

The dependency hierarchy demonstrates how Maven automatically downloads all required transitive dependencies.

---

## Learning Outcomes

- Created a Spring Boot Web project using Maven.
- Understood the standard Spring Boot project structure.
- Learned the purpose of the `@SpringBootApplication` annotation.
- Configured project dependencies using Maven.
- Explored the Maven dependency hierarchy.
- Successfully ran the application using the embedded Tomcat server.

---

## Result

The Spring Boot web application was successfully created, configured, and executed. The embedded Tomcat server started successfully on port **8080**, confirming the successful implementation of Hands-on 1.
