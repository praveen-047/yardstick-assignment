# Notes Application

## Live Demo

Explore the live application here:  
👉 [https://notes-frontend-rouge-six.vercel.app/login](https://notes-frontend-rouge-six.vercel.app/login)

---

## 🧠 Overview

This project is a full-stack Notes application built using the MERN stack (MongoDB, Express.js, React, Node.js). It allows users to:

- **Login**: Secure authentication with JWT tokens.
- **Dashboard**: Role-based access for Admin and Member users.
- **Notes Management**: Create, view, and delete notes.
- **Upgrade Plans**: Admins can upgrade tenants to the Pro plan, unlocking unlimited note creation for members.

---

## ⚙️ Tech Stack

- **Frontend**: React, React Router, Axios
- **Backend**: Node.js, Express.js, JWT Authentication
- **Database**: MongoDB
- **Styling**: CSS Modules
- **Deployment**:
  - Frontend: Vercel
  - Backend: Vercel

---

## 📁 Project Structure

/notes-app
├── /frontend
│ ├── /src
│ │ ├── /components
│ │ ├── /api.js
│ │ └── App.js
│ ├── package.json
│ └── README.md
└── /backend
├── /models
├── /routes
├── /controllers
├── server.js
└── README.md
---

## 🚀 Frontend Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/notes-app.git
   cd notes-app/frontend
Install dependencies:

bash
Copy code
npm install
Start the development server:

bash
Copy code
npm start
Access the application at http://localhost:3000.

🛠️ Backend Setup
Navigate to the backend directory:

bash
Copy code
cd notes-app/backend
Install dependencies:

bash
Copy code
npm install
Start the server:

bash
Copy code
node server.js
The backend API will be available at http://localhost:5000.

🔐 Authentication Flow
Login: Users authenticate via email and password.

JWT Tokens: Upon successful login, a JWT token is issued and stored in localStorage.

Role-Based Access:

Admin: Can view all members and upgrade tenant plans.

Member: Can create and manage their own notes.

🧪 API Endpoints
Authentication
POST /auth/login: Authenticate user and return JWT token.

Users
GET /users: Retrieve all users (Admin only).

POST /users/upgrade: Upgrade tenant to Pro plan (Admin only).

Notes
GET /notes: Retrieve all notes for the authenticated user.

POST /notes: Create a new note.

DELETE /notes/:id: Delete a note by ID.

🧩 Features
Admin Dashboard: Manage tenant users and upgrade plans.

Member Dashboard: Create and manage personal notes.

Role-Based UI: Conditional rendering based on user roles.

Persistent Login: JWT tokens stored in localStorage for session persistence.

🛠️ Development Tips
Frontend:

Ensure CORS is configured correctly in the backend to allow frontend requests.

Use useEffect hooks in React to fetch data on component mount.

Backend:

Implement middleware for JWT verification and role-based access control.

Use environment variables for sensitive information like database URIs and JWT secrets.
