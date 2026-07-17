# JUnit Basic Testing Exercises – Exercise 1: Setting Up JUnit

## Overview

This project demonstrates the basic setup of JUnit in a Maven-based Java project using IntelliJ IDEA. It is part of the Cognizant Digital Nurture Java FSE Deep Skilling program.

## Objective

- Create a Maven Java project.
- Configure JUnit 4.13.2 as a testing dependency.
- Create a simple JUnit test class.
- Execute the test successfully using IntelliJ IDEA.

## Technologies Used

- Java 22
- IntelliJ IDEA 2026
- Maven
- JUnit 4.13.2

## Project Structure

```
JUnit_Basic_Testing_Exercises
│
├── src
│   ├── main
│   │   └── java
│   └── test
│       └── java
│           └── com.cognizant
│               └── CalculatorTest.java
│
├── pom.xml
└── README.md
```

## Maven Dependency

```xml
<dependency>
    <groupId>junit</groupId>
    <artifactId>junit</artifactId>
    <version>4.13.2</version>
    <scope>test</scope>
</dependency>
```

## Test Implemented

A simple JUnit test verifies the addition of two integers using the `assertEquals()` method.

### Test Method

```java
@Test
public void testAddition() {
    int a = 10;
    int b = 20;

    int expected = 30;
    int actual = a + b;

    assertEquals(expected, actual);
}
```

## Execution Result

- JUnit dependency configured successfully.
- Test executed successfully.
- **1 test passed**.
- Process completed with **Exit Code 0**.

## Learning Outcomes

- Understanding Maven project structure.
- Configuring JUnit in a Java project.
- Writing basic JUnit test cases.
- Using assertions to validate expected results.
- Running unit tests in IntelliJ IDEA.

## Author

**Neha Sankeerthana**
