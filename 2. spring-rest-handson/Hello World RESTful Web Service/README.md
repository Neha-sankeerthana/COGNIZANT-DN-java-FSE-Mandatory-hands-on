# Hands-on 2: Hello World RESTful Web Service

## Objective
Create a simple RESTful web service using Spring Boot that returns the text **"Hello World!!"**.

## Technologies Used
- Java 21
- Spring Boot
- Spring Web
- Maven
- IntelliJ IDEA

## Project Structure

```
src
 └── main
      ├── java
      │     └── com.cognizant.springlearn
      │            ├── SpringLearnApplication.java
      │            └── controller
      │                  └── HelloController.java
      └── resources
            └── application.properties
```

## Configuration

application.properties

```properties
server.port=8083
```

## REST Endpoint

| Method | URL | Response |
|--------|------|----------|
| GET | /hello | Hello World!! |

## Running the Project

1. Open the project in IntelliJ IDEA.
2. Run `SpringLearnApplication.java`.
3. Open the browser.
4. Visit:

```
http://localhost:8083/hello
```

## Expected Output

Browser Output:

```
Hello World!!
```

Console Output:

```
Tomcat started on port 8083
Started SpringLearnApplication
```

## Learning Outcome

- Created a Spring Boot REST application.
- Implemented a REST Controller.
- Used `@RestController`.
- Used `@GetMapping`.
- Configured custom server port using `application.properties`.
- Tested the REST API in a web browser.
