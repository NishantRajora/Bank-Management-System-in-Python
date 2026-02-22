# Bank Management System (Python + MySQL CLI Application)

## Overview

This project is a console-based banking management system developed using Python with MySQL integration. It simulates core banking operations including account management, transaction processing, authentication, and database record handling.

The system is divided into two user roles:

- Administrator (bank-level control)  
- Customer (account-level operations)  

The project demonstrates practical understanding of:

- Database connectivity using mysql-connector-python  
- Structured Query Language (SQL) operations  
- Role-based access control  
- Transaction logging and data persistence  
- Command-line interface design  

---

## Project Objectives

- Implement secure login for both admin and customers  
- Perform real-time transaction processing  
- Maintain persistent transaction records  
- Manage customer accounts via relational database  
- Demonstrate structured backend application design  

---

## Core Features

### 1. Administrator Capabilities

- Open new customer account  
- Close existing account  
- View all customer records  
- View complete transaction history  
- Login with predefined credentials  

Admin has full database-level visibility and control.

---

### 2. Customer Capabilities

- Login using account number and password  
- Deposit funds  
- Withdraw funds  
- Check account balance  
- View personal transaction history  

All transactions are stored in the database for traceability.

---

### 3. Authentication System

- Role-based login (Admin / Customer)  
- Password verification from database  
- Account-number-based customer identification  

---

## Technology Stack

| Component | Technology |
|------------|------------|
| Programming Language | Python 3.x |
| Database | MySQL |
| Connector | mysql-connector-python |
| Date & Time Handling | datetime module |
| Interface | Command-Line Interface (CLI) |

---

## Database Design

Database Name: `p`

### Tables Used

1. customers  
   - Account number  
   - Name  
   - Aadhar  
   - Phone  
   - Address  
   - Balance  

2. transactions  
   - Transaction ID  
   - Account number  
   - Transaction type (Deposit/Withdraw)  
   - Amount  
   - Timestamp  

3. auth  
   - Account number  
   - Password  

The script automatically creates tables if they do not exist.

---

## Database Setup

### Step 1: Create Database

```sql
CREATE DATABASE p;
USE p;
```

Tables are auto-generated when the application runs.

---

## Default Admin Credentials

| Role  | Username | Password |
|--------|----------|----------|
| Admin  | 0        | 123      |

---

## Installation and Execution

### Step 1: Install Required Package

```
pip install mysql-connector-python
```

### Step 2: Configure MySQL Credentials

Update connection details in the script if necessary:

```python
mydb = mysql.connector.connect(
    host="localhost",
    user="root",
    passwd="your_password",
    database="p"
)
```

### Step 3: Run Application

```
python bank_system.py
```

---

## Application Flow

### Login Panel

```
1. Admin Login
2. Customer Login
```

### Admin Menu

```
1. Open New Account
2. Close Existing Account
3. View All Customer Details
4. View All Transactions
5. Log Out
```

### Customer Menu

```
1. Transaction Menu
2. Log Out
```

### Transaction Menu

```
1. Deposit
2. Withdraw
3. Balance Enquiry
4. Back to Main Menu
```

---

## Data Validation Rules

- Aadhar Number: 16 digits  
- Phone Number: 10 digits  
- Pincode: 6 digits  
- Password stored in database (currently plaintext)  

---

## System Architecture

The application follows a layered structure:

1. Presentation Layer – CLI menus and user interaction  
2. Business Logic Layer – Banking operations and validations  
3. Data Access Layer – SQL queries and database operations  
4. Persistence Layer – MySQL database  

---

## Key Learning Outcomes

- Practical experience with relational database integration  
- SQL query execution from Python  
- Role-based access control logic  
- Transaction logging system  
- Structured command-line backend development  

---

## Limitations

- Passwords are stored in plaintext  
- No encryption or hashing mechanism implemented  
- Limited exception handling  
- No concurrency control  
- Not production-ready  

This project is intended strictly for educational purposes.

---

## Future Enhancements

- Implement password hashing using bcrypt  
- Add exception handling and input validation improvements  
- Introduce transaction rollback mechanism  
- Develop GUI using Tkinter or PyQt  
- Add monthly bank statement generation  
- Export reports to PDF or Excel  
- Implement account lockout after failed login attempts  
- Add audit logging  

---

## Potential Extensions

- Convert to Flask or FastAPI backend  
- REST API integration  
- Dockerized deployment  
- Cloud database integration  
- Multi-user concurrent transaction handling  

---

## Ideal For

- Database Management System projects  
- Python + MySQL integration learning  
- Mini or Major academic projects  
- Backend fundamentals practice  

---

## Author

Nishant Rajora 
Focused on backend systems, database-driven applications, and structured programming
