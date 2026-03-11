# 📦 Inventory Management System

A simple **Inventory Management System built with Python and Excel (`openpyxl`)**.
This project allows **Admins and Employees** to manage and sell products using an Excel-based database.

The system supports **user authentication, product management, sales tracking, and bill generation**.

---

# 🚀 Features

## 🔐 Login System

* Secure login using credentials stored in **`db.xlsx`**
* Two types of users:

  * **Admin**
  * **Employee**
* Role-based menu access

---

# 👑 Admin Menu

Admin has full control over the inventory.

Options available:

1. **Add Product**
2. **Update Product**
3. **Delete Product**
4. **View Products**
5. **View Transaction History**
6. **Generate Bill / Sell Product**
7. **Logout**
8. **Exit**

---

# 👨‍💼 Employee Menu

Employee has limited access to inventory operations.

Options available:

1. **View Products**
2. **Sell Product**
3. **Generate Bill**
4. **Logout**
5. **Exit**

---

# 📊 Product Information

Each product stored in the inventory contains the following fields:

| Field    | Description               |
| -------- | ------------------------- |
| ID       | Unique product identifier |
| Name     | Product name              |
| Price    | Price per unit            |
| Quantity | Available stock           |
| GST      | Product GST percentage    |

Example:

| ID   | Name  | Price | Quantity | GST |
| ---- | ----- | ----- | -------- | --- |
| 1001 | Mouse | 500   | 20       | 18  |

---

# 🆔 Auto Product ID Generator

The system automatically generates product IDs.

Format:

```
1001
1002
1003
```

Each new product gets the **next available ID automatically**.

---

# 📁 Project Structure

```
Inventory_Management_System
│
├── main.py
├── db.xlsx
└── inventory.xlsx
```

---

# 📂 Excel Database Structure

## 1️⃣ User Database

File: **`db.xlsx`**

Sheet Name: **Users**

| user_id | username | password   | role     |
| ------- | -------- | ---------- | -------- |
|       1 | admin    | admin_pass | admin    |
|       2 | emp      | emp_pass   | employee |

---

## 2️⃣ Inventory Database

File: **`inventory.xlsx`**

### Sheet 1: Products

| ID | Name | Price | Quantity | GST |
| -- | ---- | ----- | -------- | --- |

---

### Sheet 2: Transactions

Stores product sales history.

| Date | Name | Price | Quantity | GST | Total |
| ---- | ---- | ----- | -------- | --- | ----- |

---

# ⚙️ Installation

Install the required Python library:

```bash
pip install openpyxl
```

---

# ▶️ How to Run

Run the Python file:

```bash
python main.py
```

Then login using credentials stored in **`db.xlsx`**.

---

# 🧾 Transaction History

Every time a product is sold:

* Stock is automatically reduced
* Transaction is recorded in **Transactions sheet**

Stored information includes:

* Date and time
* Product name
* Product Price
* Quantity sold
* Product GST
* Total bill amount

---

# 💡 Future Improvements

Possible upgrades for this project:

* Product search feature
* Low stock alerts
* Invoice number generation
* Better bill formatting
* Data validation


---


