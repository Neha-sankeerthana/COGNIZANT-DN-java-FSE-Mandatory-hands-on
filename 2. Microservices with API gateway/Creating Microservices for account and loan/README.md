# Microservices with API Gateway

## 📌 Overview

This project demonstrates the implementation of **Microservices with Spring Boot** and **Spring Cloud Gateway**. Two independent microservices, **Account Service** and **Loan Service**, are created and exposed through a single **API Gateway**.

The API Gateway routes incoming client requests to the appropriate microservice based on the requested endpoint.

---

## 🎯 Objective

- Develop independent Spring Boot microservices.
- Implement REST APIs for Account and Loan services.
- Configure an API Gateway using Spring Cloud Gateway.
- Route requests through a single entry point.
- Verify communication between Gateway and Microservices.

---

## 🛠 Technologies Used

- Java 21
- Spring Boot 3.3.2
- Spring Cloud Gateway
- Spring Web
- Maven
- IntelliJ IDEA
- Apache Tomcat
- Spring Boot DevTools

---

# Project Structure

```
Microservices-with-API-Gateway
│
├── account
│   ├── src
│   ├── pom.xml
│   └── application.properties
│
├── loan
│   ├── src
│   ├── pom.xml
│   └── application.properties
│
├── gateway
│   ├── src
│   ├── pom.xml
│   └── application.properties
│
├── screenshots
│   ├── 01-project-structure.png
│   ├── 02-account-running.png
│   ├── 03-loan-running.png
│   ├── 04-gateway-running.png
│   ├── 05-account-via-gateway.png
│   └── 06-loan-via-gateway.png
│
└── README.md
```

---

# Microservices

## 1. Account Service

### Port

```
8080
```

### Endpoint

```
GET /accounts/{number}
```

### Sample URL

```
http://localhost:8080/accounts/00987987973432
```

### Sample Response

```json
{
  "number": "00987987973432",
  "type": "savings",
  "balance": 234343.0
}
```

---

## 2. Loan Service

### Port

```
8081
```

### Endpoint

```
GET /loans/{number}
```

### Sample URL

```
http://localhost:8081/loans/H00987987972342
```

### Sample Response

```json
{
  "number": "H00987987972342",
  "type": "car",
  "loan": 400000.0,
  "emi": 3258,
  "tenure": 18
}
```

---

# API Gateway

The API Gateway acts as a single entry point for all client requests and forwards them to the respective microservices.

### Gateway Port

```
8082
```

### Gateway Routes

| Route | Destination |
|--------|-------------|
| /accounts/** | Account Service (8080) |
| /loans/** | Loan Service (8081) |

---

# Testing Through Gateway

## Account Service

### URL

```
http://localhost:8082/accounts/00987987973432
```

### Response

```json
{
  "number": "00987987973432",
  "type": "savings",
  "balance": 234343.0
}
```

---

## Loan Service

### URL

```
http://localhost:8082/loans/H00987987972342
```

### Response

```json
{
  "number": "H00987987972342",
  "type": "car",
  "loan": 400000.0,
  "emi": 3258,
  "tenure": 18
}
```

---

# Configuration

## Account Service

```
server.port=8080
```

## Loan Service

```
server.port=8081
```

## Gateway

```
server.port=8082
```

Configured routes:

- `/accounts/**` → Account Service
- `/loans/**` → Loan Service

---

# How to Run

### Step 1

Run the **Account Service**.

It starts on:

```
http://localhost:8080
```

---

### Step 2

Run the **Loan Service**.

It starts on:

```
http://localhost:8081
```

---

### Step 3

Run the **Gateway Service**.

It starts on:

```
http://localhost:8082
```

---

### Step 4

Access the services through the API Gateway.

```
http://localhost:8082/accounts/00987987973432
```

```
http://localhost:8082/loans/H00987987972342
```

---

# Output

Successfully verified:

- Account Microservice
- Loan Microservice
- API Gateway Routing
- REST API Responses
- Spring Cloud Gateway Configuration

---

# Screenshots

Include the following screenshots in the **screenshots/** folder:

- Project Structure
- Account Service Running
- Loan Service Running
- Gateway Running
- Account API Response via Gateway
- Loan API Response via Gateway

---

# Learning Outcomes

- Developed independent Spring Boot Microservices.
- Implemented RESTful APIs.
- Configured Spring Cloud Gateway.
- Routed requests using API Gateway.
- Tested communication between multiple services.
- Managed microservices running on different ports.

---

## Author

**Neha Sankeerthana**

**Cognizant Digital Nurture – Java FSE**

**Microservices Hands-on – API Gateway**
