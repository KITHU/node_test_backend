# Node.js MySQL Backend API

![Node.js](https://img.shields.io/badge/Node.js-v18+-green)
![Express](https://img.shields.io/badge/Express-v4.18+-lightgrey)
![MySQL](https://img.shields.io/badge/MySQL-v8.0+-blue)

![test backend](https://github.com/user-attachments/assets/d62ce86d-b37a-4f19-9e50-e8662304094f)


A RESTful API backend built with Node.js, Express, and MySQL.

## 🛠️ Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher)
- [MySQL](https://www.mysql.com/) (v8.0 or higher)
- [npm](https://www.npmjs.com/) (v9 or higher)

## 🚀 Local Setup

### 1. Clone the repository
```bash
git clone https://github.com/KITHU/node_test_backend
cd node-test-backend

npm install

mysql -u root -p

-- Create database
CREATE DATABASE node_app;

-- Create user (replace 'password' with your own)
CREATE USER 'api_user'@'localhost' IDENTIFIED BY 'password';

-- Grant privileges
GRANT ALL PRIVILEGES ON node_app.* TO 'api_user'@'localhost';

-- Create tables
USE node_app;

CREATE TABLE items (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(255) NOT NULL,
  description TEXT,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Exit MySQL
EXIT;

cp .env.example .env

```

## Edit the .env file with your credentials:


- DB_HOST=localhost
- DB_USER=api_user
- DB_PASSWORD=password  # Same as used in MySQL setup
- DB_NAME=node_app
- DB_PORT=3306
- PORT=3000

## 🏃‍♂️ Running the Application
```bash
node app.js

```
