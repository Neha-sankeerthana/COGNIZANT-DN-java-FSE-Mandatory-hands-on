# Hands-on 3: REST - Country Web Service

## Objective

Develop a RESTful web service using Spring Boot that returns the details of a country loaded from a Spring XML configuration file.

---

## Technologies Used

- Java 21
- Spring Boot
- Spring Web
- Spring Core
- Maven
- IntelliJ IDEA

---

## Project Structure

```
src
└── main
    ├── java
    │   └── com.cognizant.springlearn
    │       ├── SpringLearnApplication.java
    │       ├── Country.java
    │       └── controller
    │           ├── HelloController.java
    │           └── CountryController.java
    └── resources
        ├── application.properties
        └── country.xml
```

---

## Configuration

### application.properties

```properties
server.port=8083
```

---

### country.xml

```xml
<bean id="country"
      class="com.cognizant.springlearn.Country">

    <property name="code" value="IN"/>
    <property name="name" value="India"/>

</bean>
```

---

## REST Endpoint

| Method | URL | Response |
|--------|------|----------|
| GET | /country | Country JSON |

---

## Running the Project

1. Open the project in IntelliJ IDEA.
2. Run `SpringLearnApplication.java`.
3. Open a web browser.
4. Visit:

```
http://localhost:8083/country
```

---

## Expected Output

```json
{
  "code": "IN",
  "name": "India"
}
```

---

## Learning Outcome

- Created a RESTful web service using Spring Boot.
- Loaded bean configuration from an XML file.
- Used `ApplicationContext` and `ClassPathXmlApplicationContext`.
- Retrieved a bean using `getBean()`.
- Returned a Java object from a REST controller.
- Understood automatic JSON conversion using Jackson.
- Tested the REST API in a web browser.
