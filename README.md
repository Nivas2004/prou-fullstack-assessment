🚀 Full-Stack Inventory Management System
ProU Technology – Full-Stack Developer Assessment (Track 1, 2 & 3)

This repository contains my complete submission for the ProU Technology Full-Stack Assessment, covering:

Track 1 – Frontend (React + Mock/UI)

Track 2 – Backend (FastAPI + MongoDB)

Track 3 – Full-Stack (Integrated Web App + API + DB)

📁 Project Structure (Monorepo)
prou-fullstack-assessment/
│── frontend/        # React App (UI + Auth + Axios)
│── backend/         # FastAPI API + MongoDB
│── README.md        # Documentation

🛠 Tech Stack
Frontend

React.js

TailwindCSS

Axios

Firebase Authentication (Email + Password only)

Backend

FastAPI

Python

Motor (Async MongoDB Driver)

Pydantic

CORS Middleware

Database

MongoDB Atlas

✨ Features Implemented
Frontend

✔ Login / Signup (Email + Password)
✔ Protected Routes
✔ Add Product
✔ View Products (User-specific)
✔ Update Product
✔ Delete Product
✔ Sidebar Navigation
✔ Search & Filtering
✔ CSV Export
✔ Clean & Responsive UI

Backend

✔ Secure REST API
✔ CRUD for Products
✔ User-based data separation
✔ Full validation (numbers, IDs, missing fields)
✔ MongoDB integration
✔ CORS enabled

Full-Stack Integration

✔ React ↔ FastAPI (Axios)
✔ Firebase Auth → FastAPI user validation
✔ API authorization (each user sees only their products)

🚀 Live Demo (Optional If You Deploy)
Live Web App Link -> https://inventoryfrontend-v4ie.vercel.app/
Backend	url -> https://inventorybackend-6.onrender.com
GitHub Repository	https://github.com/Nivas2004/prou-fullstack-assessment

Project Screenshots

<div align="center">

  <!-- Image 1 -->
  <img src="https://github.com/Nivas2004/prou-fullstack-assessment/blob/main/Screenshot%202025-11-17%20201401.png?raw=true" width="700" /><br><br>

  <!-- Image 2 -->
  <img src="https://github.com/Nivas2004/prou-fullstack-assessment/blob/main/Screenshot%202025-11-17%20201101.png?raw=true" width="700" /><br><br>

  <!-- Image 3 -->
  <img src="https://github.com/Nivas2004/prou-fullstack-assessment/blob/main/Screenshot%202025-11-17%20201113.png?raw=true" width="700" />

</div>



⚙️ Setup Instructions
📦 1. Clone Repository
git clone https://github.com/Nivas2004/prou-fullstack-assessment.git
cd prou-fullstack-assessment

🎨 Frontend Setup (React)
1️⃣ Install dependencies
cd frontend
npm install
npm start

2️⃣ Configure Firebase

Create:
frontend/src/firebase.js

import { initializeApp } from "firebase/app";
import { getAuth } from "firebase/auth";

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
};

const app = initializeApp(firebaseConfig);
export const auth = getAuth(app);

3️⃣ Set Backend URL

Inside: frontend/src/api.js

export const API_URL = "http://127.0.0.1:8000";

⚙️ Backend Setup (FastAPI)
1️⃣ Create virtual environment (optional)
cd backend
pip install -r requirements.txt

2️⃣ Add environment variables

Create file: backend/.env

MONGO_URL = your-mongodb-url
DB_NAME = inventorydb

3️⃣ Start Backend Server
uvicorn app.main:app --reload


Backend runs on:

http://127.0.0.1:8000


To see API docs:

http://127.0.0.1:8000/docs

🧪 API Endpoints
Products
Method	Endpoint	Description
POST	/products/	Add product
GET	/products/user/{userId}	Get all products for user
GET	/products/{id}/{userId}	Get one product
PUT	/products/{id}/{userId}	Update product
DELETE	/products/{id}/{userId}	Delete product
🖼 Screenshots (Add When Uploading)

Login Screen

Dashboard

Add Product

Edit Product

MongoDB Collection

FastAPI Docs

🧩 Assumptions

Every user manages only their own inventory data.

Authentication is handled fully using Firebase.

Backend does not manage user accounts (only receives userId).

UI focuses on clarity and usability.

🏁 Bonus Features Implemented

Firebase authentication

Protected APIs with user ownership checks

CSV Export

Responsive UI

Complete full-stack integration

💬 Acknowledgement

This project is developed as part of the ProU Technology Full-Stack Developer Assessment.

Thank you for reviewing my submission!
