# SQL-Customer-Database
firstly create a database:
query: CREATE DATABASE gauridb1;
# Customer Orders Schema

This project contains a sample SQL schema for managing a customer order system. It includes customers, products, orders, payments, and order items.

## 📋 Tables Created

1. **Customers**
   - Stores customer details such as name, email, phone, and city.

2. **Products**
   - Stores product catalog information like name and price.

3. **Orders**
   - Records orders placed by customers with dates.

4. **Payments**
   - Tracks payment amounts and dates for each order.

5. **OrderItems**
   - Links multiple products to an order with quantity info.

## 🔗 Relationships

- Each `Order` is placed by a `Customer` (One-to-Many)
- Each `Payment` is made for an `Order` (One-to-One)
- Each `Order` can include multiple `Products` through `OrderItems` (Many-to-Many)

## 🛠 Tools Used

- **MySQL Workbench**

## 📷 ER Diagram link
![image](https://github.com/user-attachments/assets/8e18fa39-3360-4f18-ae0d-20a2ca80c6a4)

