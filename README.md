# 🏦 Bank Management System (Python + MySQL CLI App)

A **console-based banking application** built in **Python** with **MySQL** integration. This project features **admin and customer login**, **account creation**, **transactions**, and **database record management**, making it a complete simulation of a basic bank system.

---

## 🧰 Features

### 👮 Admin Features
- Open a new account  
- Close existing account  
- View all customer records  
- View all transaction records  
- Admin login (default credentials)

### 👤 Customer Features
- Log in using account number and password  
- Deposit and withdraw money  
- Balance enquiry  
- View transaction history  

### 🔐 Login System
- Admin login with fixed credentials  
- Customer login based on account number and database-stored password  

---

## 🛠️ Technologies Used

| Component       | Technology         |
|----------------|--------------------|
| Language        | Python 3.x         |
| Database        | MySQL              |
| DB Connector    | `mysql-connector-python` |
| Date Handling   | `datetime` module  |

---

## 📁 Project Structure

```
📦 BankManagementSystem/
├── bank_system.py            # Main Python script
├── MySQL Database `p`        # Pre-created with tables
└── Tables:
    ├── customers             # Stores account and personal info
    ├── transactions          # Stores deposit/withdrawal history
    └── auth                  # Stores passwords linked to acno
```

---

## 🧱 Database Setup

### 1️⃣ Create MySQL Database
```sql
CREATE DATABASE p;
USE p;
```

Tables are auto-created by the script if they don’t exist.

---

## 🔑 Default Admin Credentials

| Role   | Username | Password |
|--------|----------|----------|
| Admin  | 0        | 123      |

---

## ▶️ How to Run

### 1. Install Required Package
```bash
pip install mysql-connector-python
```

### 2. Set MySQL Credentials in Code
Update the following block if your MySQL credentials differ:
```python
mydb = mysql.connector.connect(
    host="localhost",
    user="root",
    passwd="admin@123",
    database="p"
)
```

### 3. Run the Application
```bash
python bank_system.py
```

---

## 🧪 Menu Flow

### 🔐 Login Panel
```
1. Admin Login
2. Customer Login
```

### 👮 Admin Menu
```
1. Open New Account
2. Close existing Account
3. See all Customers details
4. See all Transactions details
5. Log out
```

### 👤 Customer Menu
```
1. Transaction Menu
2. Log out
```

### 💸 Transaction Menu
```
1. Deposit
2. Withdraw
3. Balance Enquiry
4. Back to Main Menu
```

---

## 📦 Data Validation

- Aadhar: 16 digits  
- Phone Number: 10 digits  
- Pincode: 6 digits  
- Passwords stored securely in DB (plaintext — to be improved)

---

## ⚠️ Known Issues / Warnings

- ❌ Passwords are **not encrypted** (suggested: use `bcrypt`)
- ❌ No exception handling for SQL or runtime errors
- ❌ Code can be modularized for better readability

---

## 🚀 Future Enhancements

- 🔐 Encrypt customer passwords
- 📈 Add transaction history viewing per customer
- 🖥️ Develop GUI using **Tkinter** or **PyQt**
- 📊 Generate monthly bank statements
- 📤 Export data to Excel or PDF

---

## 🧑‍🏫 Ideal For

> 🎓 **Mini/Major Project** for Python + MySQL-based DBMS or Software Engineering  
> 🏫 Great for understanding file/database integration and structured programming in Python

---

## 📸 Sample Output (Screenshots)

> _Add screenshots of admin login, customer transaction, and database table views for better presentation on GitHub._

---

## 📚 References

- [MySQL Documentation](https://dev.mysql.com/doc/)
- [mysql-connector-python Docs](https://pypi.org/project/mysql-connector-python/)

---
