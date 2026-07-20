# Hands-on 4 – Difference between JPA, Hibernate and Spring Data JPA

## Objective
Understand the difference between JPA, Hibernate and Spring Data JPA by implementing a simple Spring Boot application that performs database operations using Spring Data JPA.

## Technologies Used

- Java 21
- Spring Boot 4
- Spring Data JPA
- Hibernate
- MySQL
- Maven
- IntelliJ IDEA

## Project Structure

```
src
 ├── main
 │   ├── java
 │   │    ├── model
 │   │    │     └── Employee.java
 │   │    ├── repository
 │   │    │     └── EmployeeRepository.java
 │   │    ├── service
 │   │    │     └── EmployeeService.java
 │   │    └── OrmComparisonApplication.java
 │   └── resources
 │         └── application.properties
```

## Features

- Create Employee entity
- Configure MySQL database
- Implement JpaRepository
- Use Spring Data JPA to save employee
- Demonstrate automatic transaction management
- Compare JPA, Hibernate and Spring Data JPA

## Output

```
Hibernate: select ...

Employee Saved Successfully

Process finished with exit code 0
```

## Difference

### JPA
- Java Persistence Specification
- Defines ORM standards
- No implementation

### Hibernate
- ORM Framework
- Implements JPA
- Handles database interaction

### Spring Data JPA
- Built on top of JPA
- Reduces boilerplate code
- Provides JpaRepository and CRUD methods automatically

## Result

Successfully implemented Spring Data JPA application and understood the difference between JPA, Hibernate and Spring Data JPA.
