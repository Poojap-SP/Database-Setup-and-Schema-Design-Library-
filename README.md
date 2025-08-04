# 📚 Library Management System - SQL Project

## 🎯 Objective
This project demonstrates the creation and management of a **Library Management System** using MySQL. It covers database creation, table creation with constraints, data insertion, and executing useful SQL queries for real-world operations like issuing and returning books.

---

## 🧰 Tools Used
- **Database**: MySQL
- **Client**: MySQL Workbench or any MySQL CLI

---

## 📁 Database Schema Overview

### 📌 Tables Created:
1. **Branch** – Stores information about library branches.
2. **Employee** – Stores details of employees working in each branch.
3. **Customer** – Holds registered customer information.
4. **Books** – Stores book details including ISBN, title, category, and status.
5. **IssueStatus** – Tracks books that are issued to customers.
6. **ReturnStatus** – Tracks books that have been returned.
   
### 🔐 Relationships:
- `IssueStatus` → references `Customer` and `Books` via foreign keys.
- `ReturnStatus` → references `Books`.
- `Employee` → references `Branch` (added later during query requirement).

---

## 🏗️ Features Implemented

### ✅ Data Definition:
- Used `CREATE TABLE` statements with `PRIMARY KEY`, `FOREIGN KEY`, and `ENUM`.
- Normalized table structures to reduce redundancy.

### ✅ Data Manipulation:
- Inserted sample data into all tables using `INSERT INTO`.
- Updated records using `UPDATE` (e.g., to change book availability).

### ✅ SQL Queries:
1. **Filter Available Books**  
   `SELECT book_title, category, rental_price FROM books WHERE Status = 'Yes';`
2. **Sort Employees by Salary**  
   `SELECT emp_name, salary FROM employee ORDER BY Salary DESC;`
3. **Customer-Book Issuance Report**  
   `JOIN` between `IssueStatus` and `Customer`.
4. **Book Count by Category**  
   `GROUP BY` used for category count.
5. **High Salary Employees**  
   Filter using `WHERE Salary > 50000`.
6. **Inactive Early Registrations**  
   Customers who registered before 2022 and have not issued any book.
7. **Employee Count per Branch**  
   Added `branch_no` to Employee table and used `GROUP BY`.
8. **Books Issued in June 2023**  
   `WHERE Issue_date BETWEEN '2023-06-01' AND '2023-06-30'`.
9. **Search for History Books**  
   Category-based filtering.
10. **Branches with More Than 5 Employees**  
   `HAVING` clause to filter `GROUP BY` results.

---

## 🔄 Sample Records

- 5 Branches
- 11 Employees
- 10 Customers
- 16 Books
- 5 Issued Records
- 5 Return Records

---

## 🔗 ER Diagram 
Draw the ER diagram in:
- [draw.io](https://draw.io)

---

## 🚀 How to Run
1. Open MySQL Workbench.
2. Copy and paste the SQL script from this repo.
3. Run the script step-by-step to:
   - Create the database
   - Create tables
   - Insert data
   - Execute queries

Make sure you have permission to `CREATE DATABASE`. If not, remove `CREATE DATABASE` and use an existing database with `USE your_db_name;`.

---

## 📌 Learning Outcomes
- Designed a normalized relational schema.
- Applied SQL DDL and DML statements.
- Practiced JOINS, GROUP BY, HAVING, WHERE, ORDER BY clauses.
- Understood real-world relational database use cases.




