# Exercise 2 – Implementing the Factory Method Pattern

## 📌 Overview

This project demonstrates the implementation of the **Factory Method Design Pattern** in Java.

The Factory Method Pattern is a **Creational Design Pattern** that provides an interface for creating objects without exposing the object creation logic to the client. Instead of creating objects directly using the `new` keyword, the client requests objects from a factory class.

---

## 🎯 Objective

- Understand the Factory Method Design Pattern.
- Implement a common interface for multiple classes.
- Create objects using a Factory class.
- Reduce tight coupling between the client and object creation logic.

---

## 🛠 Technologies Used

- Java
- Eclipse IDE
- JDK 21

---

## 📂 Project Structure

```
Exercise2-FactoryMethodPattern
│
├── src
│   ├── Shape.java
│   ├── Circle.java
│   ├── Rectangle.java
│   ├── ShapeFactory.java
│   └── Factory.java
│
├── screenshots
│   ├── code.png
│   └── output.png
│
└── README.md
```

---

## 📖 Factory Method Pattern

The Factory Method Pattern delegates object creation to a factory class instead of creating objects directly.

This improves:

- Code Reusability
- Maintainability
- Flexibility
- Loose Coupling

---

## 🔑 Components

### 1. Shape Interface

Defines a common method:

```java
void draw();
```

---

### 2. Circle Class

Implements the `Shape` interface.

```java
public void draw() {
    System.out.println("Drawing Circle");
}
```

---

### 3. Rectangle Class

Implements the `Shape` interface.

```java
public void draw() {
    System.out.println("Drawing Rectangle");
}
```

---

### 4. ShapeFactory Class

Creates and returns the required object based on user input.

```java
ShapeFactory factory = new ShapeFactory();

Shape shape1 = factory.getShape("CIRCLE");
Shape shape2 = factory.getShape("RECTANGLE");
```

---

### 5. Main Class

Requests objects from the factory instead of creating them directly.

```java
shape1.draw();
shape2.draw();
```

---

## ▶️ Execution

Run the `Factory.java` class.

The program:

- Creates a `ShapeFactory` object.
- Requests a `Circle` object.
- Requests a `Rectangle` object.
- Calls the `draw()` method for each object.

---

## ✅ Expected Output

```
Drawing Circle
Drawing Rectangle
```

---

## 📊 Explanation

- The client does not create `Circle` or `Rectangle` objects directly.
- The `ShapeFactory` decides which object to instantiate.
- This approach hides object creation logic from the client and promotes loose coupling.

---

## 📸 Screenshots

Include the following screenshots:

- Project Structure
- Shape Interface
- Circle Class
- Rectangle Class
- ShapeFactory Class
- Main Class
- Program Output

---

## 📚 Learning Outcomes

- Understood the Factory Method Design Pattern.
- Implemented interfaces and polymorphism.
- Created objects through a Factory class.
- Reduced dependency between client code and concrete classes.
- Improved code maintainability and scalability.

---

## 👩‍💻 Author

**Neha Sankeerthana**

**Cognizant Digital Nurture – Java FSE**

**Exercise 2 – Implementing the Factory Method Pattern**
