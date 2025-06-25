# 👤 Customers Table – E-Commerce MySQL Database (gauridb1)
---

## 📂 Database Name

`gauridb1`

---

## 📋 Table: Customers

The `Customers` table stores the personal information of buyers, including their contact details and location.

### 🧱 Structure

| Column Name | Data Type    | Description                         |
|-------------|--------------|-------------------------------------|
| customer_id | INT (PK)     | Unique customer ID (auto-increment) |
| name        | VARCHAR(100) | Full name of the customer           |
| email       | VARCHAR(100) | Email address (unique)              |
| phone       | VARCHAR(15)  | Contact number                      |
| city        | VARCHAR(50)  | City of residence                   |

### 💻 SQL Definition

```sql
CREATE TABLE Customers (
    customer_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE,
    phone VARCHAR(15),
    city VARCHAR(50)
);
🔗 Table Relationship
A single Customer can place multiple Orders

This relationship is defined using the customer_id foreign key in the Orders table.

📊 Entity Relationship Diagram (ERD) – Customers Table
mermaid
Copy
Edit
erDiagram
    Customers ||--o{ Orders : places

    Customers {
        INT customer_id PK
        VARCHAR name
        VARCHAR email
        VARCHAR phone
        VARCHAR city
    }

    Orders {
        INT order_id PK
        INT customer_id FK
        DATE order_date
    }
🧪 Sample Queries
🔍 View All Customers
sql
Copy
Edit
SELECT * FROM Customers;
🔍 Customers from a Specific City
sql
Copy
Edit
SELECT * FROM Customers WHERE city = 'Delhi';

🛠 Tools Used
MySQL Workbench
GitHub

📊 ER Diagram – Customers Domain
https://drive.google.com/file/d/1FpOU3emMp9F2mW6cRYy51ftZwEjz3O3U/view?usp=sharing
