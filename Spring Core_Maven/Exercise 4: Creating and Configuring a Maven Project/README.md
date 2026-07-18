# Exercise 4 – Creating and Configuring a Maven Project

## Objective

The objective of this exercise is to create a Maven-based Spring project and configure it with the required Spring Framework dependencies and Maven Compiler Plugin. This exercise demonstrates how Maven simplifies dependency management and project configuration.

---

## Scenario

A new **Library Management System** project needs to be created using **Apache Maven**. The project should include the necessary Spring Framework libraries and be configured to compile Java source code using the Maven Compiler Plugin.

---

## Technologies Used

- Java
- Apache Maven
- Spring Framework
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
    │   └── resources
    │
    └── test
```

---

## Maven Dependencies

The following Spring dependencies were added to the `pom.xml` file:

### Spring Context

```xml
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-context</artifactId>
    <version>5.3.39</version>
</dependency>
```

### Spring AOP

```xml
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-aop</artifactId>
    <version>5.3.39</version>
</dependency>
```

### Spring Web MVC

```xml
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-webmvc</artifactId>
    <version>5.3.39</version>
</dependency>
```

---

## Maven Compiler Plugin

The Maven Compiler Plugin is configured to compile the project using **Java 1.8**.

```xml
<build>
    <plugins>

        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-compiler-plugin</artifactId>
            <version>3.11.0</version>

            <configuration>
                <source>1.8</source>
                <target>1.8</target>
            </configuration>

        </plugin>

    </plugins>
</build>
```

---

## Implementation Steps

1. Create a new Maven project named **LibraryManagement**.
2. Add the required Spring Framework dependencies:
   - Spring Context
   - Spring AOP
   - Spring Web MVC
3. Configure the Maven Compiler Plugin for Java 1.8.
4. Reload the Maven project to download all dependencies.
5. Verify that the dependencies appear under **External Libraries** in IntelliJ IDEA.

---

## Verification

After reloading the Maven project, the following Spring libraries should be available:

- spring-context
- spring-aop
- spring-beans
- spring-core
- spring-expression
- spring-jcl
- spring-web
- spring-webmvc

---

## Expected Result

- Maven project created successfully.
- Spring dependencies downloaded successfully.
- Maven Compiler Plugin configured.
- Project builds successfully without dependency errors.
- Required Spring libraries are available in **External Libraries**.

---

## Concepts Covered

- Apache Maven
- Maven Project Structure
- Dependency Management
- Spring Framework Dependencies
- Maven Compiler Plugin
- Build Configuration
- Project Configuration

---

## Learning Outcomes

- Create a Maven-based Java project.
- Manage project dependencies using Maven.
- Configure the Maven Compiler Plugin.
- Integrate Spring Framework libraries into a Maven project.
- Understand Maven's standard project structure and dependency resolution.

---

## Conclusion

This exercise demonstrates how to create and configure a Maven project for a Spring application. By using Maven for dependency management and build configuration, developers can efficiently manage project libraries, simplify builds, and maintain a consistent project structure.
