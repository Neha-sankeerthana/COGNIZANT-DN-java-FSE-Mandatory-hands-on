# Exercise 1 – Implementing the Singleton Pattern

## 📌 Overview

This project demonstrates the implementation of the **Singleton Design Pattern** in Java.

The Singleton Pattern is a creational design pattern that ensures only **one instance** of a class is created throughout the application's lifecycle while providing a global access point to that instance.

---

## 🎯 Objective

- Understand the Singleton Design Pattern.
- Create a class that allows only one object to be instantiated.
- Access the same object using a static method.
- Verify that multiple references point to the same instance.

---

## 🛠 Technologies Used

- Java
- Eclipse IDE
- JDK 21

---

## 📂 Project Structure

```
Exercise1-SingletonPattern
│
├── src
│   ├── Singleton.java
│   └── Single.java
│
├── screenshots
│   ├── code.png
│   └── output.png
│
└── README.md
```

---

## 📖 Singleton Pattern

The Singleton Pattern ensures that:

- Only one object of a class exists.
- The object is created only when needed (Lazy Initialization).
- The same object is returned whenever requested.

---

## 🔑 Key Features

### 1. Private Constructor

Prevents creating objects using the `new` keyword.

```java
private Singleton() {
    System.out.println("Singleton Object Created");
}
```

---

### 2. Static Instance Variable

Stores the single instance of the class.

```java
private static Singleton instance;
```

---

### 3. Static Factory Method

Returns the existing object if already created; otherwise creates a new one.

```java
public static Singleton getInstance() {
    if (instance == null) {
        instance = new Singleton();
    }
    return instance;
}
```

---

## ▶️ Execution

Run the `Single.java` class.

The program creates two references:

```java
Singleton obj1 = Singleton.getInstance();
Singleton obj2 = Singleton.getInstance();
```

Then compares them:

```java
System.out.println(obj1 == obj2);
```

---

## ✅ Expected Output

```
Singleton Object Created
true
```

---

## 📊 Explanation

- The message **"Singleton Object Created"** is printed only once because the object is created only during the first call to `getInstance()`.
- The comparison `obj1 == obj2` returns **true**, proving that both references point to the same object.

---

## 📸 Screenshots

Include the following screenshots:

- Project Structure
- Singleton Class Code
- Main Class Code
- Program Output

---

## 📚 Learning Outcomes

- Understood the Singleton Design Pattern.
- Implemented lazy initialization.
- Restricted object creation using a private constructor.
- Used a static method to access the singleton instance.
- Verified that only one object exists throughout the application.

---

## 👩‍💻 Author

**Neha Sankeerthana**

**Cognizant Digital Nurture – Java FSE**

**Exercise 1 – Implementing the Singleton Pattern**
