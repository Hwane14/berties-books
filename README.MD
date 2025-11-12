# Bertie's Books

**Bertie's Books** is a dynamic Node.js web application for managing a bookshop inventory. Users can browse available books, add new entries, register, and search the catalog using exact or partial matches. It demonstrates Express routing, EJS templating, and MySQL integration.

---

## 🛠️ Technologies Used

- **Node.js** with **Express.js** — server-side framework
- **EJS** — templating engine for dynamic HTML
- **MySQL** — relational database for storing book data
- **CSS** — custom styling via `main.css`

---

## 🚦 Available Routes

| Route                   | Description                            |
|------------------------|----------------------------------------|
| `/`                    | Homepage with navigation               |
| `/about`               | About the shop                         |
| `/search`              | Form to search for books               |
| `/register`            | User registration page                 |
| `/books/addbook`       | Form to add a new book                 |
| `/list`                | Displays all books in the database     |
| `/books/bargainbooks`  | Lists books priced below a set amount |

---

## 🔍 Advanced Search Feature

The `/search` route supports **partial matching** using SQL `LIKE` queries. For example, searching for `"World"` will return:

- *Brave New World*
- *Atlas of the World*
- *World History*

This allows users to find books even if they only remember part of the title.

---

## 🧪 How to Install and Run Locally

### 1. Clone the Repository

```bash
git clone https://github.com/Hwane14/06_berties_33821100
cd berties-books
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Set up the Database
Open MySQL and run:
```Sql
SOURCE create_db.sql;
SOURCE insert_test_data.sql;
```

Create the app user:
```Sql
CREATE USER IF NOT EXISTS 'berties_books_app'@'localhost' IDENTIFIED BY 'qwertyuiop';
GRANT ALL PRIVILEGES ON mybookshop.* TO 'berties_books_app'@'localhost';
```

### 4. Start the Server
```bash
node index.js
```
Visit http://localhost:8000 in your browser