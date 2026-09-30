# Backend Server

A REST API backend built with **Node.js, Express.js, MongoDB, and Mongoose**.

## 📌 Project Overview

This backend provides the server-side functionality for the application, including API routes, database connectivity, authentication, and data management.

## 🚀 Technologies

* Node.js
* Express.js
* MongoDB
* Mongoose
* JWT
* bcryptjs
* CORS
* dotenv
* Nodemon

## 📁 Project Structure

```text
server/
│
├── src/
│   ├── config/
│   │   └── db.js
│   │
│   ├── controllers/
│   │
│   ├── middleware/
│   │
│   ├── models/
│   │
│   ├── routes/
│   │
│   ├── utils/
│   │
│   └── server.js
│
├── .env
├── .gitignore
├── package.json
├── package-lock.json
└── README.md
```

## ⚙️ Installation

Clone the repository:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Go to the server directory:

```bash
cd server
```

Install dependencies:

```bash
npm install
```

## 🔐 Environment Variables

Create a `.env` file in the server root directory:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
CLIENT_URL=http://localhost:5173
NODE_ENV=development
```

> Never upload the `.env` file to GitHub.

## ▶️ Run the Server

### Development

```bash
npm run dev
```

The server will run on:

```text
http://localhost:5000
```

### Production

```bash
npm start
```

## 🧪 API Testing

You can test the backend API using:

* Postman
* Thunder Client
* Insomnia

### Server Test

Open:

```text
GET http://localhost:5000
```

Expected response:

```text
Server is running
```

### Example API Endpoints

| Method | Endpoint             | Purpose         |
| ------ | -------------------- | --------------- |
| GET    | `/api/users`         | Get users       |
| GET    | `/api/users/:id`     | Get single user |
| POST   | `/api/auth/register` | Register user   |
| POST   | `/api/auth/login`    | Login user      |
| GET    | `/api/profile`       | Get profile     |
| PUT    | `/api/profile`       | Update profile  |
| DELETE | `/api/users/:id`     | Delete user     |

> Update these endpoints according to the actual routes implemented in the project.

## 🧪 Testing Workflow

### 1. Start the server

```bash
npm run dev
```

### 2. Check server response

```text
http://localhost:5000
```

### 3. Test API with Postman

For example:

```text
POST http://localhost:5000/api/auth/register
```

Example JSON body:

```json
{
  "name": "MD Riad Bhuiyan",
  "email": "riad@example.com",
  "password": "123456"
}
```

Then test login:

```text
POST http://localhost:5000/api/auth/login
```

Example:

```json
{
  "email": "riad@example.com",
  "password": "123456"
}
```

## 🔒 Authentication

The application uses **JWT (JSON Web Token)** for authentication.

Passwords are securely hashed using **bcryptjs** before being stored in the database.

## 🗄️ Database

This project uses:

```text
MongoDB
```

with:

```text
Mongoose
```

for database interaction.

## 📦 Available Scripts

```bash
# Start development server
npm run dev

# Start production server
npm start
```

## 🌐 API Base URL

### Local Development

```text
http://localhost:5000
```

### Production

Add your deployed backend URL here after deployment:

```text
https://your-backend-url.com
```

## 🛡️ Security

* `.env` is excluded from Git.
* Passwords are hashed using bcryptjs.
* JWT is used for authentication.
* CORS is configured for frontend communication.
* Sensitive credentials should never be committed to GitHub.

## 📝 Git

Before committing:

```bash
git status
```

Add files:

```bash
git add .
```

Commit:

```bash
git commit -m "Initial backend setup"
```

Push:

```bash
git push origin main
```

## 👨‍💻 Author

**MD Riad Bhuiyan**

## 📄 License

This project is licensed under the ISC License.
