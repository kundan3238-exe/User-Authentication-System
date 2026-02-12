# User Authentication System

## 📌 Project Overview
This project implements a secure **User Authentication System** for a web application using **Node.js, Express, MongoDB, and JWT**. It supports user registration, login, password hashing, and protected routes using token-based authentication.

The project was developed as **Task 2** of a Web Development Internship.

---

## 🛠️ Tech Stack
- Node.js
- Express.js
- MongoDB (MongoDB Atlas)
- Mongoose
- JSON Web Tokens (JWT)
- bcryptjs
- dotenv

---

## ✨ Features
- User Registration
- User Login
- Password Hashing using bcrypt
- JWT-based Authentication
- Protected Routes using Middleware
- Secure handling of environment variables

---

## 📂 Project Structure
user-authentication-system/
│
├── config/
│ └── db.js
│
├── models/
│ └── User.js
│
├── routes/
│ └── authRoutes.js
│
├── middleware/
│ └── authMiddleware.js
│
├── index.js
├── .env
└── .gitignore

---

## ⚙️ Setup & Installation

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/user-authentication-system.git
cd user-authentication-system

2️⃣ Install Dependencies
npm install

3️⃣ Configure Environment Variables

Create a .env file in the root directory and add:

PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret

4️⃣ Run the Server
npm run dev


Server will start on:

http://localhost:5000

🔐 API Endpoints
🟢 Register User

POST /api/auth/register

Body (JSON):

{
  "name": "Test User",
  "email": "test@example.com",
  "password": "123456"
}

🔵 Login User

POST /api/auth/login

Body (JSON):

{
  "email": "test@example.com",
  "password": "123456"
}


Response:

{
  "token": "JWT_TOKEN"
}

🔒 Protected Route

GET /api/auth/dashboard

Headers:

Authorization: Bearer <JWT_TOKEN>

🔑 Authentication Flow

User registers with email and password

Password is hashed before saving to database

User logs in and receives a JWT token

Token is sent in the Authorization header

Middleware verifies token before allowing access to protected routes

🚫 Security Measures

Passwords are hashed using bcrypt

JWT used for stateless authentication

Sensitive data stored using environment variables

Protected routes secured using middleware

🧪 Testing

All endpoints were tested locally using Postman / Thunder Client.

✅ Task Status

✔ Task completed successfully
✔ All required objectives implemented
✔ Authentication flow verified

📌 Note

Deployment was not required as per task instructions. The system was implemented and tested in a local development environment.

👨‍💻 Author

Kundan Atel
