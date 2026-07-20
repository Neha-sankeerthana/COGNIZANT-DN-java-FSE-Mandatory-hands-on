# Exercise 7 – Financial Forecast Using Recursion

## 📌 Overview

This project demonstrates a **Financial Forecasting** application developed in Java using the **Recursion** algorithm.

The program predicts the future financial value based on a fixed annual growth rate by recursively applying the growth percentage for a specified number of years.

---

## 🎯 Objective

- Understand recursion in Java.
- Forecast future financial values using a recursive approach.
- Analyze the time and space complexity of recursive algorithms.

---

## 🛠 Technologies Used

- Java
- Eclipse IDE
- JDK 21

---

## 📂 Project Structure

```
FinancialForecast
│
├── src
│   └── FinancialForecast.java
│
├── screenshots
│   ├── code.png
│   └── output.png
│
└── README.md
```

---

## 📖 Algorithm Used

### Recursion

The recursive function repeatedly applies the annual growth rate until the required number of years becomes zero.

### Steps

1. Read the current financial value.
2. Read the annual growth rate.
3. Read the number of years.
4. Apply the growth rate recursively.
5. Stop recursion when the number of years becomes zero.
6. Display the forecasted financial value.

---

## 💻 Program Logic

The recursive function follows this approach:

```java
forecast(currentValue, growthRate, years)
```

If years become zero, the current value is returned.

Otherwise,

```java
forecast(currentValue * (1 + growthRate), growthRate, years - 1);
```

---

## ▶️ Sample Input

```
Current Value : 10000
Growth Rate (%) : 5
Years : 2
```

---

## ✅ Sample Output

```
Future Value after 2 years = 11025.00
```

---

## ⏱ Complexity Analysis

| Complexity | Value |
|------------|-------|
| Time Complexity | O(n) |
| Space Complexity | O(n) (Recursive Call Stack) |

---

## 📸 Screenshots

Include the following screenshots in your repository:

- Project Structure
- Source Code
- Program Output

---

## 📚 Learning Outcomes

- Learned the concept of recursion.
- Implemented recursive algorithms in Java.
- Forecasted financial values using compound growth.
- Understood recursive base case and recursive calls.
- Analyzed time and space complexity of recursion.

---

## 👩‍💻 Author

**Neha Sankeerthana**

**Cognizant Digital Nurture – Java FSE**

**Exercise 7 – Financial Forecast Using Recursion**
