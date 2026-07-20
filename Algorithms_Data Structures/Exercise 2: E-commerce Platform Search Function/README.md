# Exercise 2 – E-commerce Platform Search Function

## 📌 Overview

This project implements an **E-commerce Product Search System** in Java using the **Binary Search** algorithm.

The application stores product information in an array, sorts the products alphabetically by product name, and efficiently searches for a product using Binary Search.

---

## 🎯 Objective

- Implement Binary Search in Java.
- Compare Linear Search and Binary Search.
- Improve search efficiency by sorting data before searching.
- Understand the time complexity of different searching algorithms.

---

## 🛠 Technologies Used

- Java
- Eclipse IDE
- JDK 21

---

## 📂 Project Structure

```
EcommerceSearch
│
├── src
│   ├── Product.java
│   └── SearchFunction.java
│
├── screenshots
│   ├── code.png
│   ├── output.png
│   └── project-structure.png
│
└── README.md
```

---

## 📖 Algorithm Used

### Binary Search

Binary Search works by repeatedly dividing the sorted array into two halves until the target product is found.

---

## 🔄 Program Workflow

1. Create a **Product** class containing:
   - Product ID
   - Product Name
   - Category
2. Store product details in an array.
3. Sort the array based on Product Name.
4. Apply Binary Search to locate the desired product.
5. Display the product details if found.
6. Otherwise, display **"Product Not Found"**.

---

## ▶️ Sample Products

| Product ID | Product Name | Category |
|------------|--------------|-----------|
| 101 | Laptop | Electronics |
| 102 | Phone | Electronics |
| 103 | Shoes | Fashion |
| 104 | Watch | Accessories |

---

## ▶️ Sample Search

```
Search Product : Phone
```

---

## ✅ Sample Output

```
Product Found

ID: 102
Name: Phone
Category: Electronics
```

---

## ⏱ Complexity Analysis

| Algorithm | Time Complexity |
|-----------|-----------------|
| Linear Search | O(n) |
| Binary Search | O(log n) |

> Binary Search is significantly faster than Linear Search for large, sorted datasets.

---

## 📸 Screenshots

Include the following screenshots in your GitHub repository:

- Project Structure
- Java Source Code
- Program Output

---

## 📚 Learning Outcomes

- Learned how Binary Search works.
- Understood the importance of sorting before searching.
- Compared Linear Search and Binary Search.
- Improved search efficiency using divide-and-conquer.
- Analyzed time complexity of searching algorithms.

---

## 👩‍💻 Author

**Neha Sankeerthana**

**Cognizant Digital Nurture – Java FSE**

**Exercise 2 – E-commerce Platform Search Function**
