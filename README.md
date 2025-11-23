# 🔐 User Account Creation System (AWS Lambda + Redis + React)

A full-stack user account management system with:

- **Backend:** Python Flask API on **AWS Lambda** using **Serverless Framework**
- **Database:** **Redis (AWS ElastiCache / Redis OSS Serverless)**
- **Frontend:** **React + React-Bootstrap** dashboard
- **Hosting:** Backend via AWS API Gateway, Frontend on **Netlify**

---

## 🌐 Live Demo

- 🖥 **Dashboard (Frontend):**  
  👉 https://user-creation-app.netlify.app/

- ⚙️ **API Base URL (Backend):**  
  👉 `https://owf5o8rlm8.execute-api.ap-south-1.amazonaws.com/dev`

---

## ✅ Features

### Backend (Flask + Lambda)
- CRUD API for User Accounts:
  - `POST /users` – Create user
  - `GET /users/{email}` – Get single user
  - `GET /users` – List all users
  - `PUT /users/{email}` – Update user
  - `DELETE /users/{email}` – Delete user
- Uses Redis hashes to store:
  - `email`, `first_name`, `last_name`, `password (hashed)`
- Deployed with **Serverless Framework** to AWS Lambda & API Gateway
- VPC + Security Groups configured to access Redis

### Frontend (React + React-Bootstrap)
- Responsive **Account Management Dashboard**
- Left sidebar with sections:
  - **User Profile** (connected to live API – full CRUD)
  - **Notifications**
  - **Billing & Invoices**
  - **Plans & Add-ons**
- Uses **Axios** to call the deployed API

---

## 🧱 Project Structure

```bash
user-account-creation-project/
│
├── flask-lambda-redis-api/        # Backend - Flask + Lambda + Redis
│   ├── app.py                     # Flask app + Lambda handler
│   ├── serverless.yml             # Serverless Framework config
│   ├── requirements.txt           # Python dependencies
│
└── user-account-dashboard/        # Frontend - React + React-Bootstrap
    ├── src/App.js                 # Dashboard UI + API integration
    ├── src/index.js               # React entry + Bootstrap import
    ├── package.json
