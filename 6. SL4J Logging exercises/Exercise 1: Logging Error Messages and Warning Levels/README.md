# Exercise 1 – Logging Error Messages and Warning Levels using SLF4J

## Objective

The objective of this exercise is to learn how to use **SLF4J (Simple Logging Facade for Java)** with **Logback** to log messages at different severity levels, specifically **ERROR** and **WARN**.

---

## Scenario

A Java application needs to record important runtime events using a logging framework instead of printing messages to the console. This exercise demonstrates logging error and warning messages using SLF4J.

---

## Technologies Used

- Java
- Maven
- SLF4J
- Logback
- IntelliJ IDEA

---

## Project Structure

```
SLF4J_Logging_Exercises
│
├── pom.xml
│
└── src
    └── main
        └── java
            └── com.cognizant
                └── Main.java
```

---

## Dependencies

```xml
<dependency>
    <groupId>org.slf4j</groupId>
    <artifactId>slf4j-api</artifactId>
    <version>1.7.30</version>
</dependency>

<dependency>
    <groupId>ch.qos.logback</groupId>
    <artifactId>logback-classic</artifactId>
    <version>1.2.3</version>
</dependency>
```

---

## Implementation

### Create Logger

```java
private static final Logger logger =
        LoggerFactory.getLogger(Main.class);
```

---

### Log Error Message

```java
logger.error("This is an error message");
```

---

### Log Warning Message

```java
logger.warn("This is a warning message");
```

---

## Program Flow

1. Configure SLF4J and Logback dependencies using Maven.
2. Create a Logger instance using `LoggerFactory`.
3. Log an ERROR level message.
4. Log a WARN level message.
5. Observe the formatted log output in the console.

---

## Expected Output

```
ERROR com.cognizant.Main - This is an error message

WARN com.cognizant.Main - This is a warning message

Process finished with exit code 0
```

---

## Learning Outcomes

- Understand the purpose of SLF4J.
- Configure Logback as the logging implementation.
- Create and use Logger objects.
- Log messages using different logging levels.
- Understand the difference between ERROR and WARN logs.

---

## Conclusion

This exercise demonstrates how to integrate SLF4J with Logback in a Maven-based Java project. Logging provides a structured and configurable way to record application events, making debugging, monitoring, and maintenance much easier than using standard console output.
