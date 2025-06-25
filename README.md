# 👤 Customers Table – E-Commerce MySQL Database (gauridb1)

This document highlights the **Customers** domain within the `gauridb1` MySQL e-commerce database. It captures essential buyer details and their direct relationship with the order system.

---

## 📂 Database Name

`gauridb1`

---

## 📋 Table: Customers

The **Customers** table is responsible for storing user information such as their full name, email, phone number, and city. It includes unique identifiers for each customer and supports optional fields like phone and city to allow flexibility in data entry.

---

## 🔗 Table Relationship

Each customer can place **multiple orders**, establishing a one-to-many relationship with the **Orders** table. This linkage ensures that the database can track purchases made by any individual customer efficiently.

---

## 🧪 Sample Use Cases

- Viewing the complete list of customers.
- Filtering customers by city or location.
- Checking which customers have placed orders.
- Performing analysis like customer count per city or activity level.

---

## 🛠 Tools Used

- **MySQL Workbench** – for designing and managing the database structure.
- **GitHub** – for version control and project sharing.

---

## 📊 ER Diagram – Customers Domain

The structure and relationship of the **Customers** table can be viewed in the ER diagram linked below:

👉 [View ER Diagram on Google Drive](https://drive.google.com/file/d/1FpOU3emMp9F2mW6cRYy51ftZwEjz3O3U/view?usp=sharing)

---
## 🙋‍♀️ Author

**Gauri Milind Javheri**  
Internship Project – Customers Table | `gauridb1`
