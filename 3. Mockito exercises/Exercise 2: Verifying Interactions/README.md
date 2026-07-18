# Exercise 2 – Verifying Interactions using Mockito

## Objective
The objective of this exercise is to learn how to verify interactions between a service class and its dependency using **Mockito**. Instead of checking the returned value, this exercise verifies whether a specific method is invoked on a mock object.

## Scenario
A service (`MyService`) depends on an external API (`ExternalApi`). The goal is to verify that the `getData()` method of the external API is called when the `fetchData()` method of the service is executed.

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
            └── MyServiceVerificationTest.java
```

## Technologies Used

- Java
- JUnit 4
- Mockito
- Maven
- IntelliJ IDEA

## Files Description

### ExternalApi.java
Defines an interface representing an external service.

```java
public interface ExternalApi {
    String getData();
}
```

### MyService.java
Contains a service class that depends on `ExternalApi`.

```java
public String fetchData() {
    return api.getData();
}
```

### MyServiceVerificationTest.java
Implements a unit test using Mockito to verify that the `getData()` method is invoked when `fetchData()` is executed.

## Test Execution Steps

1. Create a mock object for `ExternalApi`.
2. Inject the mock object into `MyService`.
3. Call the `fetchData()` method.
4. Verify that the `getData()` method of the mock object is invoked using Mockito's `verify()` method.

## Expected Output

```
Tests passed: 1
Process finished with exit code 0
```

## Key Mockito Method Used

```java
verify(mockApi).getData();
```

This statement verifies that the `getData()` method was called exactly once during the execution of the test.

## Learning Outcomes

- Understand interaction testing using Mockito.
- Learn how to verify method invocations with `verify()`.
- Test service behavior without depending on external implementations.
- Improve confidence in unit testing by ensuring expected interactions occur.

## Conclusion

This exercise demonstrates how Mockito's `verify()` method can be used to confirm that a service correctly interacts with its dependencies. Verifying interactions is an essential part of unit testing, ensuring that methods are invoked as expected while keeping tests isolated from external systems.
