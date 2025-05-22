#  User Access Management System

A role-based software access system with authentication, access requests, and approvals — built using **Node.js**, **React**, **TypeORM**, **PostgreSQL**, and **JWT**.

---

##  Features

-  User Registration & Login with JWT Authentication
-  Role-based Access: Employee, Manager, Admin
-  Software Management (Create, List)
-  Access Requests (Employees)
- Approve/Reject Requests (Managers)

---

## Tech Stack

| Layer      | Tech                          |
|------------|-------------------------------|
| Frontend   | React, Axios, React Router    |
| Backend    | Node.js, Express.js           |
| ORM        | TypeORM                       |
| Database   | PostgreSQL                    |
| Auth       | JWT, bcrypt                   |
| Tooling    | dotenv, nodemon, cors         |

---

## User Roles & Permissions

| Role     | Permissions                                                       |
|----------|-------------------------------------------------------------------|
| Employee | Sign up, log in, request access to software                       |
| Manager  | Log in, view/approve/reject access requests                       |
| Admin    | Log in, create software, full system access                       |

---

## Project Structure
user-access-management-system/
├── client/ # React frontend
│ ├── src/
│ │ ├── pages/ # All role-based pages
│ │ └── App.js # Routing based on roles
├── server/ # Node backend
│ ├── entities/ # TypeORM entities
│ ├── index.js # Entry point
│ └── data-source.js # TypeORM DB config
├── .gitignore
├── README.md
└── package.json


---

##  Getting Started

### 1️Clone the repository


git clone https://github.com/valli1354/user-access-management-system.git
cd user-access-management-system

Backend Setup:
---------------------

cd server
npm install

 Create .env in server/:
-----------------------------
env

PORT=5000
DB_HOST=localhost
DB_PORT=5432
DB_USERNAME=your_postgres_username
DB_PASSWORD=your_postgres_password
DB_DATABASE=user_access_system
JWT_SECRET=your_secret_key

 Run the server:
-------------------
npm run dev

 Frontend Setup:
-----------------------------------
cd ../client
npm install
npm start

API Endpoints:
------------------------
Auth
POST /api/auth/signup – Register as Employee

POST /api/auth/login – Login and receive JWT

Software (Admin):
-------------------------
POST /api/software – Add software

 Requests (Employee & Manager):
------------------------------------------
POST /api/requests – Request access

GET /api/requests – List pending requests (Manager)

PATCH /api/requests/:id – Approve/Reject

 Pages:
-------------
Path	Component	Role
/signup	Signup.js	Everyone
/login	Login.js	Everyone
/create-software	CreateSoftware.js	Admin
/request-access	RequestAccess.js	Employee
/pending-requests	PendingRequests.js	Manager

Author:
------------------------------
GitHub Profile-valli1354

