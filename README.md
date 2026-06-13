# 🍕 Pizza Sales Dashboard | Power BI

## 📌 Project Overview

This project presents an interactive Pizza Sales Dashboard built using Power BI. The dashboard analyzes transactional sales data and provides insights into customer ordering behavior, sales performance, and product popularity.

---

## 📊 Key Performance Indicators

* Total Sales
* Total Orders
* Total Pizzas Sold
* Average Order Value

---

## 📈 Dashboard Insights

### Total Sales by Category

Analyze revenue contribution across pizza categories.

### Monthly Sales Trend

Track sales performance over time.

### Top 10 Best-Selling Pizzas

Identify the highest revenue-generating pizzas.

### Total Sales by Day

Understand sales patterns across weekdays.

### Total Sales by Size

Analyze customer preference for pizza sizes.

### Orders by Hour

Identify peak ordering hours.

---

## 🗂 Dataset

The dashboard is built using four tables:

1. Orders
2. Order Details
3. Pizzas
4. Pizza Types

---

## 🔗 Data Model

orders (1) ──── (*) order_details (*) ──── (1) pizzas (*) ──── (1) pizza_types

---

## ⚙️ DAX Measures

### Total Sales

```DAX
Total Sales =
SUMX(
    order_details,
    order_details[quantity] * RELATED(pizzas[price])
)
```

### Total Orders

```DAX
Total Orders =
DISTINCTCOUNT(orders[order_id])
```

### Total Pizzas Sold

```DAX
Total Pizzas Sold =
SUM(order_details[quantity])
```

### Average Order Value

```DAX
Average Order Value =
DIVIDE([Total Sales], [Total Orders])
```

---

## 🛠 Tools Used

* Power BI
* DAX
* Data Modeling
* Data Visualization

---

## 🎯 Skills Demonstrated

* Data Cleaning
* Data Modeling
* Relationship Management
* DAX Calculations
* Dashboard Design
* Business Intelligence
* Analytical Thinking

---

## 📷 Dashboard Preview

(Add dashboard screenshot here)

---

## ⭐ If you found this project interesting, feel free to star the repository and connect with me on LinkedIn!
