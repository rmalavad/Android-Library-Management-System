# Android Library Management System

**Author:** Ruturaj Malavade  
**Project Type:** Database Management System (DBMS) Laboratory Project  
**Team Size:** 2  
**Frontend:** Android (PHP, HTML, JavaScript)  
**Backend:** MySQL  

---

## 📘 Overview

This project implements an advanced **Library Management System** capable of managing multiple library branches, tracking all books, employees, and customers through a centralized database.  
Developed as part of a DBMS laboratory project, it demonstrates the design and deployment of a **multi-user, role-based** library system integrated with an **Android front end** and **MySQL** backend.

The system supports **three user roles**:
- **Administrators:** Manage all employees and system-wide data.  
- **Employees:** Manage books, customers, and branch-level transactions.  
- **Customers:** Search books, issue or return borrowed items, and view personal history.

---

## 🧠 Database Design

The database schema is designed for normalization and scalability, ensuring accurate relational mapping between key entities.

### **Entities and Attributes**

| Entity | Key Attributes | Description |
|--------|----------------|--------------|
| **Book** | Book_ID, Title, Author, Publisher, Edition, Status, Category | Stores complete book metadata and current status (issued / available). |
| **Customer** | Customer_ID, Name, Address, Registration_Date, Books_Issued, Fine | Records all customer information and loan activity. |
| **Branch** | Branch_ID, Address, Manager_ID, Contact_Number | Represents each library branch managed by a specific employee. |
| **Employee** | Employee_ID, Name, Salary, Position | Tracks staff details and roles (manager / staff). |
| **TransactionStatus** | Transaction_ID, Customer_ID, Book_ID, TransType, Trans_Date | Logs all issue and return transactions with fine tracking. |

**Relationships:**  
- A **Manager** manages one **Branch** (1–N)  
- A **Customer** registers at one **Branch** (N–1)  
- A **Customer** transacts many **Books** (N–1)  
- An **Employee** updates many **Books** (N–N)

---

## ⚙️ Tech Stack

- **Frontend:** PHP, HTML, JavaScript (served via Android web-view)  
- **Backend:** MySQL  
- **Tools Used:** phpMyAdmin, MySQL Workbench  
- **Platform:** Android Studio / Localhost WebView  

---

## 🔑 Core Features

- 📚 **Book Management:** Add, update, and search for books across branches.  
- 👥 **User Authentication:** Concurrent logins for administrators, employees, and customers.  
- 🧾 **Issue & Return Tracking:** Record every transaction with due dates and fine calculation.  
- 🏢 **Branch-Level Management:** Each branch linked to a manager from the employee database.  
- 💼 **Employee Oversight:** Administrators can view and manage all staff records.  
- 🌐 **Portability:** Android interface provides mobile access to all system functionalities.  

---

## 🚀 Setup & Usage

1. Import the SQL schema into **MySQL** using `phpMyAdmin` or `MySQL Workbench`.  
2. Deploy project files to your local server directory (e.g., `/htdocs` for XAMPP).  
3. Start Apache and MySQL services.  
4. Access the project either via browser or Android WebView application.  

---

## 📄 Documentation

The complete **database schema** and **ER diagram** are included in the [synopsis.docx](./synopsis.docx) file, which details:
- Entity–Relationship Diagram  
- Normalized schema  
- Functional requirements  
- Data types and constraints used in each table  
