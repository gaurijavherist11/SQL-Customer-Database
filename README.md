# 🛒 E-Commerce MySQL Database – gauridb1

This project demonstrates a simple e-commerce backend database using **MySQL**, designed as part of an internship task. It covers the complete flow from customer registration, order placement, product management, and payments.

## 📂 Database Name

`gauridb1`

---

## 📋 Tables Included

- **Customers**: Stores buyer information including name, contact, and city.
- **Products**: Contains the catalog with product names and prices.
- **Orders**: Tracks each order placed by a customer.
- **Payments**: Records payment details per order.
- **OrderItems**: Links orders to products, with quantity per item.

---

## 🔗 Table Relationships

- Each **Customer** can place many **Orders**.
- Each **Order** is linked to one **Payment**.
- Each **Order** can contain multiple **OrderItems**.
- Each **OrderItem** refers to one **Product**.

---

## 📊 Entity Relationship Diagram (ERD)
file:///C:/Users/gauri/Downloads/ER-Diagram_of_customerdb.pdf
