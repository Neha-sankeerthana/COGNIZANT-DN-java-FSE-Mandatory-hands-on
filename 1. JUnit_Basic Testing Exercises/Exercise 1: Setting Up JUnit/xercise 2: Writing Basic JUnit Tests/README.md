# JUnit Basic Testing Exercises – Exercise 2: Writing Basic JUnit Tests

## Overview

This project demonstrates how to write and execute basic JUnit test cases for a simple Java class. It is part of the Cognizant Digital Nurture Java FSE Deep Skilling Program.

## Objective

- Create a Java class with basic arithmetic operations.
- Write JUnit test cases for each method.
- Validate the results using JUnit assertions.
- Execute all test cases successfully.

## Technologies Used

- Java 22
- IntelliJ IDEA
- Maven
- JUnit 4.13.2

## Project Structure

```
JUnit_Basic_Testing_Exercises
│
├── src
│   ├── main
│   │   └── java
│   │       └── com.cognizant
│   │           └── Calculator.java
│   │
│   └── test
│       └── java
│           └── com.cognizant
│               └── CalculatorTest.java
│
├── pom.xml
└── README.md
```

## Calculator Methods

The `Calculator` class contains the following methods:

- add(int a, int b)
- subtract(int a, int b)
- multiply(int a, int b)
- divide(int a, int b)

## Test Cases Implemented

| Test Method | Description |
|-------------|-------------|
| testAddition() | Verifies addition operation |
| testSubtraction() | Verifies subtraction operation |
| testMultiplication() | Verifies multiplication operation |
| testDivision() | Verifies division operation |

## Assertions Used

- `assertEquals()`

## Execution Result

- Total Tests Executed: **4**
- Tests Passed: **4**
- Tests Failed: **0**
- Build Status: **SUCCESS**
- Process Finished with Exit Code **0**

## Learning Outcomes

- Creating Java classes for testing
- Writing JUnit test methods
- Using the `@Test` annotation
- Validating outputs using `assertEquals()`
- Executing multiple JUnit test cases using IntelliJ IDEA

## Author

**Neha Sankeerthana**
