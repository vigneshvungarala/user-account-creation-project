# 🚀 User Account Creation System

A full-stack **User Account Management System** built with a scalable serverless architecture using AWS services and a modern React dashboard.

---

## 🧩 Project Overview

This system allows complete CRUD operations for user accounts through a secure backend API and an intuitive frontend dashboard.

### 🔗 Live Demo

* 🖥 **Application:**
  [https://user-creation-app.netlify.app/](https://user-creation-app.netlify.app/)

* ⚙️ **Backend API Base URL:**
  [https://owf5o8rlm8.execute-api.ap-south-1.amazonaws.com/dev/health](https://owf5o8rlm8.execute-api.ap-south-1.amazonaws.com/dev)

---

## ✅ Features

### 🔧 Backend (Flask + AWS Lambda)

* RESTful CRUD API for User Accounts:

  * `POST /users` – Create user
  * `GET /users/{email}` – Get single user
  * `GET /users` – Get all users
  * `PUT /users/{email}` – Update user
  * `DELETE /users/{email}` – Delete user
* Redis used for data storage with hashes:

  * email
  * first_name
  * last_name
  * password (hashed)
* Serverless deployment using **Serverless Framework**
* Secure VPC & Security Group configuration for Redis access

### 🎨 Frontend (React + React-Bootstrap)

* Responsive Account Management Dashboard
* Sidebar Navigation:

  * User Profile (Full CRUD)
  * Notifications
  * Billing & Invoices
  * Plans & Add-ons
* API integration via Axios
* Hosted on Netlify

---

## 🏗 Project Structure

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
```

---

## 🧠 System Architecture

```
User Browser
     │
     ▼
React Dashboard (Netlify)
     │
Axios HTTP Requests
     ▼
AWS API Gateway
     ▼
AWS Lambda (Flask API)
     ▼
Redis Database (AWS ElastiCache)
```

---

## 🧪 Run Locally

### 🔹 Backend (Flask)

```bash
cd flask-lambda-redis-api
pip install -r requirements.txt

# Start local Redis or update REDIS_HOST in app.py
python app.py
```

API will run at:
👉 [http://localhost:5000](http://localhost:5000)

---

### 🔹 Frontend (React)

```bash
cd user-account-dashboard
npm install
npm start
```

App will run at:
👉 [http://localhost:3000](http://localhost:3000)

---

## 🔌 API Endpoints

| Method | Endpoint       | Description   |
| ------ | -------------- | ------------- |
| POST   | /users         | Create user   |
| GET    | /users/{email} | Fetch user    |
| GET    | /users         | Get all users |
| PUT    | /users/{email} | Update user   |
| DELETE | /users/{email} | Delete user   |

---

## 🧰 Technology Stack

### Backend

* Python
* Flask
* AWS Lambda
* API Gateway
* Serverless Framework
* Redis (ElastiCache Serverless)

### Frontend

* React.js
* React-Bootstrap
* Axios
* Netlify Hosting

---

## 📈 Key Achievements

✔ Fully serverless architecture
✔ Live production deployment
✔ Secure Redis integration
✔ Responsive dashboard UI
✔ Scalable and modular codebase
✔ Real-world recruitment-level implementation

---

## Author

**Vignesh**
Aspiring software Developer
B.Tech passout (2025)

Built as part of a recruitment task to demonstrate:

* Backend API Development
* Serverless Cloud Deployment
* Database Integration
* Frontend Dashboard Development

---

## 📬 Contact

For feedback, improvements, or collaboration:

* LinkedIn :https://www.linkedin.com/in/vigneshvungarala/

---

## ✅ Project Status

 * Project Complete
 * Live
 * Production Ready


