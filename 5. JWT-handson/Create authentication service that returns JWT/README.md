# JWT Authentication Service

## Overview

This project demonstrates the implementation of **JWT (JSON Web Token) Authentication** using **Spring Boot** and **Spring Security**. It is developed as part of the **Cognizant Digital Nurture Java FSE** hands-on exercises.

The application authenticates a user using **HTTP Basic Authentication** and generates a **JWT token** upon successful authentication.

---

## Technologies Used

- Java 21
- Spring Boot 3.3.2
- Spring Security
- Spring Web
- Maven
- JJWT 0.11.5

---

## Project Structure

```
jwt-authentication-service
│
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com.cognizant.jwtauthenticationservice
│   │   │       ├── config
│   │   │       │   └── SecurityConfig.java
│   │   │       ├── controller
│   │   │       │   └── AuthenticationController.java
│   │   │       ├── util
│   │   │       │   └── JwtUtil.java
│   │   │       └── JwtAuthenticationServiceApplication.java
│   │   └── resources
│   │       └── application.properties
│   └── test
│
├── pom.xml
└── README.md
```

---

## Features

- Spring Boot REST API
- Spring Security Configuration
- HTTP Basic Authentication
- JWT Token Generation
- Secure Authentication Endpoint
- Maven-based Project Structure

---

## Dependencies

- Spring Boot Starter Web
- Spring Boot Starter Security
- JJWT API
- JJWT Impl
- JJWT Jackson
- Spring Boot DevTools

---

## Configuration

**application.properties**

```properties
server.port=8081
```

---

## Default Credentials

| Username | Password |
|----------|----------|
| user | pwd |

---

## API Endpoint

### Generate JWT Token

**Request**

```
GET /authenticate
```

Example:

```
http://localhost:8081/authenticate
```

Authentication Type:

```
Basic Authentication
```

Credentials:

```
Username : user
Password : pwd
```

---

## Sample Response

```json
{
  "token": "eyJhbGciOiJIUzI1NiJ9..."
}
```

---

## How to Run

1. Clone the repository.

```
git clone https://github.com/your-username/jwt-authentication-service.git
```

2. Open the project in IntelliJ IDEA.

3. Update Maven dependencies.

4. Run:

```
JwtAuthenticationServiceApplication.java
```

5. Open your browser or Postman.

```
http://localhost:8081/authenticate
```

6. Authenticate using:

```
Username : user
Password : pwd
```

7. The application returns a JWT token.

---

## Output

```
{
   "token":"eyJhbGciOiJIUzI1NiJ9..."
}
```

---

## Learning Outcomes

- Configure Spring Security
- Implement Basic Authentication
- Generate JWT Tokens
- Build Secure REST APIs
- Understand Stateless Authentication
- Integrate JJWT with Spring Boot

---

## Author

**Neha Sankeerthana**

Cognizant Digital Nurture Program – Java Full Stack Engineer (Java FSE)

---
