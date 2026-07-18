# Exercise 1 – Mocking and Stubbing using Mockito

## Objective
The objective of this exercise is to understand how to use **Mockito** to create mock objects and stub method responses while writing unit tests with **JUnit**.

## Scenario
A service (`MyService`) depends on an external API (`ExternalApi`). Instead of calling the real API during testing, Mockito is used to create a mock implementation and return predefined data.

## Project Structure

```
src
├── main
│   └── java
│       └── com.cognizant
│           ├── ExternalApi.java
│           └── MyService.java
│
└── test
    └── java
        └── com.cognizant
            └── MyServiceTest.java
```

## Technologies Used

- Java
- JUnit 4
- Mockito
- Maven
- IntelliJ IDEA

## Files Description

### ExternalApi.java
Defines an interface with a method:

```java
String getData();
```

### MyService.java
Contains a service class that depends on `ExternalApi`.

```java
public String fetchData() {
    return api.getData();
}
```

### MyServiceTest.java
Implements unit testing using Mockito by:
- Creating a mock object
- Stubbing the `getData()` method
- Injecting the mock into the service
- Verifying the returned result using JUnit assertions

## Test Execution Steps

1. Create a mock object using Mockito.
2. Stub the method to return `"Mock Data"`.
3. Pass the mock object to `MyService`.
4. Call `fetchData()`.
5. Verify the returned value using `assertEquals()`.

## Expected Output

```
Tests passed: 8
Process finished with exit code 0
```

## Learning Outcomes

- Understand Mockito mocking.
- Learn method stubbing using `when().thenReturn()`.
- Perform unit testing using JUnit.
- Test service classes without calling external dependencies.
- Improve test isolation and reliability.

## Conclusion

This exercise demonstrates how Mockito simplifies unit testing by replacing external dependencies with mock objects. It ensures that the service logic is tested independently without relying on real API implementations.
