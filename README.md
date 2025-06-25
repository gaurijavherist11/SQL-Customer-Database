use gauridb1;

-- 1. Customer Table
CREATE TABLE Customers (
    customer_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE,
    phone VARCHAR(15),
    city VARCHAR(50)
);

-- 2. Product Table
CREATE TABLE Products (
    product_id INT PRIMARY KEY AUTO_INCREMENT,
    product_name VARCHAR(100) NOT NULL,
    price DECIMAL(10, 2) NOT NULL
);

-- 3. Orders Table
CREATE TABLE Orders (
    order_id INT PRIMARY KEY AUTO_INCREMENT,
    customer_id INT,
    order_date DATE,
    FOREIGN KEY (customer_id) REFERENCES Customers(customer_id)
);

-- 4. Payment table 
CREATE TABLE Payments (
    payment_id INT PRIMARY KEY AUTO_INCREMENT,
    order_id INT,
    amount_paid DECIMAL(10, 2),
    payment_date DATE,
    FOREIGN KEY (order_id) REFERENCES Orders(order_id)
);


-- 5. OrderItems table
CREATE TABLE OrderItems (
    order_item_id INT PRIMARY KEY AUTO_INCREMENT,
    order_id INT,
    product_id INT,
    quantity INT,
    FOREIGN KEY (order_id) REFERENCES Orders(order_id),
    FOREIGN KEY (product_id) REFERENCES Products(product_id)
);





INSERT INTO Customers (name, email, phone, city) VALUES
('Amit Mehra', 'amit1@email.com', '9000010001', 'Mumbai'),
('Sara Khan', 'sara2@email.com', '9000010002', 'Delhi'),
('Ravi Patel', 'ravi3@email.com', '9000010003', 'Ahmedabad'),
('Pooja Sharma', 'pooja4@email.com', '9000010004', 'Pune'),
('Ramesh Iyer', 'ramesh5@email.com', '9000010005', 'Chennai'),
('Priya Verma', 'priya6@email.com', '9000010006', 'Bangalore'),
('Zoya Sheikh', 'zoya7@email.com', '9000010007', 'Hyderabad'),
('Nikhil Jain', 'nikhil8@email.com', '9000010008', 'Jaipur'),
('Anjali Roy', 'anjali9@email.com', '9000010009', 'Kolkata'),
('Arjun Rao', 'arjun10@email.com', '9000010010', 'Nagpur'),
('Vikram Singh', 'vikram11@email.com', '9000010011', 'Surat'),
('Neha Gupta', 'neha12@email.com', '9000010012', 'Indore'),
('Siddharth Das', 'sid13@email.com', '9000010013', 'Lucknow'),
('Sneha Nair', 'sneha14@email.com', '9000010014', 'Thane'),
('Raj Malhotra', 'raj15@email.com', '9000010015', 'Nashik'),
('Meena Joshi', 'meena16@email.com', '9000010016', 'Bhopal'),
('Kunal Deshmukh', 'kunal17@email.com', '9000010017', 'Noida'),
('Ishita Mehra', 'ishita18@email.com', '9000010018', 'Ghaziabad'),
('Tushar Kapoor', 'tushar19@email.com', '9000010019', 'Kanpur'),
('Kavita Yadav', 'kavita20@email.com', '9000010020', 'Varanasi');

INSERT INTO Products (product_name, price) VALUES
('Laptop', 55000.00),
('Smartphone', 25000.00),
('Monitor', 8000.00),
('Keyboard', 1200.00),
('Mouse', 700.00),
('Headphones', 1800.00),
('Webcam', 2300.00),
('Tablet', 30000.00),
('Printer', 10000.00),
('Smartwatch', 6000.00),
('Gaming Console', 45000.00),
('Speakers', 3500.00),
('USB Cable', 150.00),
('Hard Drive', 5000.00),
('Power Bank', 2000.00),
('LED Strip', 300.00),
('Microphone', 2500.00),
('Bluetooth Adapter', 800.00),
('SSD 1TB', 7500.00),
('RAM 16GB', 6500.00);

INSERT INTO Orders (customer_id, order_date) VALUES
(1, '2024-06-01'),
(2, '2024-06-02'),
(3, '2024-06-03'),
(4, '2024-06-04'),
(5, '2024-06-05'),
(6, '2024-06-06'),
(7, '2024-06-07'),
(8, '2024-06-08'),
(9, '2024-06-09'),
(10, '2024-06-10'),
(11, '2024-06-11'),
(12, '2024-06-12'),
(13, '2024-06-13'),
(14, '2024-06-14'),
(15, '2024-06-15'),
(16, '2024-06-16'),
(17, '2024-06-17'),
(18, '2024-06-18'),
(19, '2024-06-19'),
(20, '2024-06-20'),
(1, '2024-06-21'),
(2, '2024-06-22'),
(3, '2024-06-23'),
(4, '2024-06-24'),
(5, '2024-06-25'),
(6, '2024-06-26'),
(7, '2024-06-27'),
(8, '2024-06-28'),
(9, '2024-06-29'),
(10, '2024-06-30');

INSERT INTO Payments (order_id, amount_paid, payment_date) VALUES
(1, 55000.00, '2024-06-02'),
(2, 25000.00, '2024-06-03'),
(3, 8000.00, '2024-06-04'),
(4, 1200.00, '2024-06-05'),
(5, 700.00, '2024-06-06'),
(6, 1800.00, '2024-06-07'),
(7, 2300.00, '2024-06-08'),
(8, 30000.00, '2024-06-09'),
(9, 10000.00, '2024-06-10'),
(10, 6000.00, '2024-06-11'),
(11, 45000.00, '2024-06-12'),
(12, 3500.00, '2024-06-13'),
(13, 150.00, '2024-06-14'),
(14, 5000.00, '2024-06-15'),
(15, 2000.00, '2024-06-16'),
(16, 300.00, '2024-06-17'),
(17, 2500.00, '2024-06-18'),
(18, 800.00, '2024-06-19'),
(19, 7500.00, '2024-06-20'),
(20, 6500.00, '2024-06-21'),
(21, 1200.00, '2024-06-22'),
(22, 6000.00, '2024-06-23'),
(23, 3000.00, '2024-06-24'),
(24, 999.00, '2024-06-25'),
(25, 2999.00, '2024-06-26'),
(26, 3499.00, '2024-06-27'),
(27, 2500.00, '2024-06-28'),
(28, 1550.00, '2024-06-29'),
(29, 4900.00, '2024-06-30'),
(30, 2400.00, '2024-07-01');

INSERT INTO OrderItems (order_id, product_id, quantity) VALUES
(1, 1, 2),
(2, 3, 1),
(3, 5, 3),
(4, 7, 2),
(5, 2, 1),
(6, 4, 2),
(7, 6, 1),
(8, 8, 3),
(9, 9, 2),
(10, 10, 1),
(11, 11, 2),
(12, 12, 1),
(13, 13, 3),
(14, 14, 1),
(15, 15, 2),
(16, 16, 1),
(17, 17, 2),
(18, 18, 3),
(19, 19, 1),
(20, 20, 2);

SELECT * FROM customers;
SELECT * FROM  orders;
SELECT * FROM payments;
SELECT * FROM OrderItems;
SELECT * FROM products;
