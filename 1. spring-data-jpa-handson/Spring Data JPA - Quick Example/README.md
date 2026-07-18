# Spring Data JPA - Hands-on 1

## Overview
This project demonstrates the basic implementation of **Spring Data JPA** with **Spring Boot** and **MySQL**. It retrieves data from a MySQL database using the Repository-Service architecture and displays the results in the console.

## Technologies Used
- Java 21
- Spring Boot
- Spring Data JPA
- Maven
- MySQL
- IntelliJ IDEA

## Project Structure

```
src
└── main
    ├── java
    │   └── com.cognizant.ormlearn
    │       ├── model
    │       │   └── Country.java
    │       ├── repository
    │       │   └── CountryRepository.java
    │       ├── service
    │       │   └── CountryService.java
    │       └── OrmLearnApplication.java
    └── resources
        └── application.properties
```

## Database Setup

Create the database:

```sql
CREATE DATABASE ormlearn;
USE ormlearn;
```

Create the table:

```sql
CREATE TABLE country(
    co_code VARCHAR(2) PRIMARY KEY,
    co_name VARCHAR(50)
);
```

Insert sample data:

```sql
INSERT INTO country VALUES ('IN','India');
INSERT INTO country VALUES ('US','United States of America');
```

## Configuration

Configure the database connection in `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/ormlearn
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

spring.jpa.hibernate.ddl-auto=validate
```

## Features

- Spring Boot project setup
- Spring Data JPA integration
- Entity mapping using JPA annotations
- Repository interface using JpaRepository
- Service layer implementation
- MySQL database connectivity
- Fetching all country records using `findAll()`

## Expected Output

```
Start

Hibernate:
select co_code, co_name from country;

countries=[
Country{code='IN', name='India'},
Country{code='US', name='United States of America'}
]

End
```

## Learning Outcomes

- Create a Spring Boot application using Spring Initializr.
- Configure MySQL with Spring Boot.
- Map Java classes to database tables using JPA annotations.
- Implement Repository and Service layers.
- Retrieve records from a database using Spring Data JPA.
- Execute and verify database operations through application logs.

## Author

**Neha Sankeerthana**
