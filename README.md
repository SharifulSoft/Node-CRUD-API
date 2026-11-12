# 🧩 Node CRUD API

A simple, beginner-friendly **full-stack CRUD application** for managing users. It has a REST API built with **Node.js, Express and MongoDB**, and a **React + Vite** client to create, list, update and delete users.

![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white)

---

## ✨ Features

- ➕ **Create** a user (name and email)
- 📄 **Read** all users
- ✏️ **Update** an existing user
- 🗑️ **Delete** a user
- Client-side routing with React Router
- Clean REST endpoints that are easy to test with Postman or any REST client

## 🛠 Tech Stack

| Layer    | Technology                          |
|----------|-------------------------------------|
| Frontend | React, React Router, Vite, CSS      |
| Backend  | Node.js, Express, CORS, dotenv      |
| Database | MongoDB (official `mongodb` driver) |

## 📁 Project Structure

```
Node-CRUD-API/
├── server-side/          # Express REST API
│   ├── index.js
│   └── .env.example
└── client-side/          # React + Vite client
    └── src/
        ├── App.jsx       # Add-user form
        └── components/   # UserShow (list/delete), Updated (edit)
```

## 🚀 Getting Started

### Prerequisites
- Node.js 18 or newer
- A MongoDB connection string (for example, from [MongoDB Atlas](https://www.mongodb.com/atlas))

### 1. Clone the repository
```bash
git clone https://github.com/SharifulSoft/Node-CRUD-API.git
cd Node-CRUD-API
```

### 2. Start the backend
```bash
cd server-side
npm install
cp .env.example .env      # then set MONGODB_URI to your own connection string
npm start
```
The API runs at **http://localhost:5000**.

### 3. Start the frontend
```bash
cd ../client-side
npm install
npm run dev
```
Open the URL Vite prints, usually **http://localhost:5173**.

## 🔐 Environment Variables (`server-side/.env`)

| Variable      | Description                    |
|---------------|--------------------------------|
| `MONGODB_URI` | Your MongoDB connection string |
| `PORT`        | API port (default `5000`)      |

## 📡 API Endpoints

| Method | Endpoint        | Description            |
|--------|-----------------|------------------------|
| GET    | `/users`        | Get all users          |
| POST   | `/users`        | Create a user          |
| GET    | `/update/:id`   | Get a single user      |
| PUT    | `/update/:id`   | Update a user          |
| DELETE | `/users/:id`    | Delete a user          |

**Example request:**
```bash
curl -X POST http://localhost:5000/users \
  -H "Content-Type: application/json" \
  -d '{"name": "John Doe", "email": "john@example.com"}'
```

## 👤 Author

**SharifulSoft**: [github.com/SharifulSoft](https://github.com/SharifulSoft)

⭐ If you find this project useful, please give it a star!
