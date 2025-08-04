# 🛍️ Simple E-Commerce DB Schema

This project represents a basic **E-Commerce Database Design** using SQL, including two core entities: **Customers** and **Orders**. It demonstrates the use of **Primary and Foreign Keys**, and models a real-world one-to-many relationship between customers and their orders.

---

## 📌 Project Overview

- **Domain:** E-Commerce
- **Entities:** Customers, Orders
- **Relationship:** One Customer → Many Orders
- **Database Used:** SQL Server (works with MySQL/PostgreSQL too)

---

## 🧱 Database Tables

### 🔹 1. Customers Table

| Column Name | Data Type     | Description                       |
|-------------|---------------|-----------------------------------|
| CustomerID  | INT (PK)      | Unique ID for each customer       |
| Name        | VARCHAR(100)  | Customer's full name              |
| Email       | VARCHAR(100)  | Customer's unique email address   |

### 🔹 2. Orders Table

| Column Name | Data Type     | Description                       |
|-------------|---------------|-----------------------------------|
| OrderID     | INT (PK)      | Unique ID for each order          |
| CustomerID  | INT (FK)      | References `Customers(CustomerID)`|
| OrderDate   | DATE          | Date when the order was placed    |
| TotalAmount | DECIMAL(10,2) | Total price of the order          |

---

## 🔗 Relationships

- One **Customer** can place many **Orders**
- Implemented using a **foreign key**:
  - `Orders.CustomerID` → `Customers.CustomerID`
---

