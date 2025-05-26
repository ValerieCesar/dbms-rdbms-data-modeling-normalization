-- Create tables for a sample database

CREATE TABLE departments (
    dept_id INT PRIMARY KEY,
    dept_name VARCHAR(100),
    dept_location VARCHAR(100)
);


![Image](https://github.com/user-attachments/assets/0e086056-55cd-4922-ba91-20e0b82c1c35)

CREATE TABLE employees (
    emp_id INT PRIMARY KEY,
    emp_name VARCHAR(100),
    dept_id INT,
    salary DECIMAL(10, 2),
    FOREIGN KEY (dept_id) REFERENCES departments(dept_id)
);

![Image](https://github.com/user-attachments/assets/efe15d15-6ecf-47b7-b368-4688bef7be4d)

CREATE TABLE products (
    product_id INT PRIMARY KEY,
    product_name VARCHAR(100),
    price DECIMAL(10, 2)
);

![Image](https://github.com/user-attachments/assets/4d4269de-1466-4f1b-9013-c216510ea6d5)
