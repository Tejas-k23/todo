# 📝 Task Tracker App

A full-stack Task Tracker application built using the MERN stack. This app allows users to register, log in, and manage their tasks in a clean and intuitive UI.

## 🔧 Tech Stack

- **Frontend**: React.js
- **Backend**: Node.js, Express.js
- **Database**: MySQL
- **Authentication**: JWT & Bcrypt
- **Environment Configuration**: dotenv

## 📁 Folder Structure

/client → React frontend code
/server → Node.js + Express backend code

yaml

---

## ⚙️ How to Install and Run

### 🔹 Frontend (React)

```bash
cd client
npm install
npm start
🔹 Backend (Express)
bash

cd server
npm install
npm start
Make sure .env file is configured properly.

🗂️ MySQL Setup
Create a MySQL Database named task_tracker

Use the following SQL to create the required table:

sql

CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(255),
  email VARCHAR(255) UNIQUE,
  password VARCHAR(255)
);
You can also create a tasks table if used:

sql

CREATE TABLE tasks (
  id INT AUTO_INCREMENT PRIMARY KEY,
  user_id INT,
  title VARCHAR(255),
  completed BOOLEAN DEFAULT FALSE,
  FOREIGN KEY (user_id) REFERENCES users(id)
);
📦 Environment Configuration
Include a .env.example file in both client and server folders.

Example: .env.example (server)
env

PORT=5000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=yourpassword
DB_NAME=task_tracker
JWT_SECRET=your_jwt_secret

🚀 Run Locally (Both)
In separate terminals:

bash

# Backend
cd server
npm install
npm start

# Frontend
cd client
npm install
npm start
