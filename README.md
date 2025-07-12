# 🛒 E-commerce Web App using Express, EJS, Bootstrap with PostgreSQL

This is a full-stack E-commerce web application built using **Express.js**, **EJS**, and **Bootstrap**, with **PostgreSQL** as the relational database. It enables users to create accounts, browse categorized products (groceries, electronics, clothing), add to cart, and securely place orders.

---

## 🚀 Features

- 🛍️ Product browsing: Grocery, Clothing, Electronics
- ➕ Add and remove items from cart
- 🔐 User signup & login
- 📦 Order review and checkout
- 📄 Stores order & user details in PostgreSQL
- 📃 Admin-friendly schema for product tracking
- 🧠 EJS templates with Bootstrap styling
- 🔐 dotenv for environment variables

---

## 🛠️ Tech Stack

- **Frontend**: EJS, HTML, Bootstrap
- **Backend**: Express.js, Node.js
- **Database**: PostgreSQL
- **Authentication**: Basic login system (can be extended with JWT & bcrypt)
- **Environment Handling**: dotenv
- **Version Control**: Git & GitHub

---

## 📁 Folder Structure

```
project-root/
│
├── public/              --> Static files (CSS/images)
├── views/               --> EJS templates (index, login, signup, etc.)
├── grocery.json         --> Static grocery product data
├── clothing.json        --> Static clothing product data
├── electronics.json     --> Static electronics product data
├── index.js             --> Main Express app
├── .env                 --> Environment variables (ignored by Git)
├── .gitignore
├── package.json
└── package-lock.json
```

---

## 🧑‍💻 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

---

### 2. Install dependencies

```bash
npm install
```

---

### 3. Set up environment variables

Create a `.env` file in the root directory:

```env
DB_USER=your_postgres_user
DB_HOST=localhost
DB_NAME=your_database
DB_PASSWORD=your_password
DB_PORT=5432
```

---

### 4. Run the development server

```bash
nodemon index.js
```

The app will run locally at:  
📍 http://localhost:3000

---

## 🧩 PostgreSQL Table Setup

### `signup`
```sql
CREATE TABLE signup (
  email VARCHAR(255) PRIMARY KEY,
  password TEXT
);
```

### `customer`
```sql
CREATE TABLE customer (
  c_id SERIAL PRIMARY KEY,
  email VARCHAR(255),
  fullname TEXT,
  address TEXT
);
```

### `order_items`
```sql
CREATE TABLE order_items (
  id SERIAL PRIMARY KEY,
  c_id INT,
  p_name TEXT,
  price INT
);
```

---

## 🙏 Acknowledgements

Special thanks to open-source contributors and maintainers of Express.js, PostgreSQL, and Bootstrap for enabling this build.

---
