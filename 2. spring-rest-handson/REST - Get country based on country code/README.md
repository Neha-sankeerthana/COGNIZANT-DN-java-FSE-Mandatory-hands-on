# REST - Get Country Based on Country Code

## 📌 Overview
This project is a Spring Boot RESTful Web Service that returns country details based on the country code provided in the URL. The country information is loaded from an XML configuration file (`country.xml`) using Spring's `ApplicationContext`. The service performs a case-insensitive search and returns the matching country details in JSON format.

---

## 🛠️ Technologies Used

- Java 21
- Spring Boot
- Spring Web MVC
- Spring Core (XML Configuration)
- Maven
- IntelliJ IDEA

---

## 📁 Project Structure

```
spring-learn
│
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com.cognizant.springlearn
│   │   │       ├── controller
│   │   │       │   └── CountryController.java
│   │   │       ├── service
│   │   │       │   └── CountryService.java
│   │   │       ├── Country.java
│   │   │       └── SpringLearnApplication.java
│   │   │
│   │   └── resources
│   │       ├── application.properties
│   │       └── country.xml
│   │
│   └── test
│
├── pom.xml
└── README.md
```

---

## 🚀 Features

- Develops a RESTful Web Service using Spring Boot.
- Loads country data from an XML configuration file.
- Retrieves country details using the country code.
- Supports case-insensitive country code matching.
- Returns JSON responses automatically using Jackson.
- Follows MVC architecture.

---

## 🌐 REST API

### Get Country by Country Code

**Request Method**

```
GET
```

**Endpoint**

```
/country/{code}
```

### Sample Requests

```
http://localhost:8083/country/IN
```

```
http://localhost:8083/country/in
```

```
http://localhost:8083/country/US
```

```
http://localhost:8083/country/DE
```

```
http://localhost:8083/country/JP
```

---

## ✅ Sample Responses

### India

```json
{
  "code": "IN",
  "name": "India"
}
```

### United States

```json
{
  "code": "US",
  "name": "United States"
}
```

### Germany

```json
{
  "code": "DE",
  "name": "Germany"
}
```

### Japan

```json
{
  "code": "JP",
  "name": "Japan"
}
```

---

## ⚙️ Implementation Details

### Controller

- Exposes the REST endpoint `/country/{code}`.
- Accepts the country code using `@PathVariable`.
- Invokes the service layer to retrieve country information.

### Service

- Loads the list of countries from `country.xml`.
- Performs a case-insensitive search using `equalsIgnoreCase()`.
- Returns the matching `Country` object.

### XML Configuration

The `country.xml` file stores all available country beans configured using Spring XML.

### JSON Conversion

Spring Boot automatically converts the returned `Country` object into JSON using the Jackson library.

---

## ▶️ How to Run

1. Clone the repository.
2. Open the project in IntelliJ IDEA.
3. Update Maven dependencies.
4. Ensure the following property is present:

```properties
server.port=8083
```

5. Run:

```
SpringLearnApplication.java
```

6. Open a browser or Postman.

7. Test the API using:

```
http://localhost:8083/country/IN
```

---

## 📷 Expected Output

| Request | Response |
|---------|----------|
| `/country/IN` | India |
| `/country/US` | United States |
| `/country/DE` | Germany |
| `/country/JP` | Japan |

---

## 🎯 Learning Outcomes

- Spring Boot REST API Development
- Spring MVC Annotations
- XML Bean Configuration
- Spring ApplicationContext
- Dependency Injection
- Path Variables
- JSON Serialization using Jackson
- Maven Project Structure

---

## ✅ Result

Successfully implemented a Spring Boot RESTful Web Service that retrieves country details based on the country code. The application loads data from an XML configuration file, performs a case-insensitive search, and returns the matching country information in JSON format.
