#  User Account Creation System (AWS Lambda + Redis + React)

A full-stack user account management system with:

- **Backend:** Python Flask API on **AWS Lambda** using **Serverless Framework**
- **Database:** **Redis (AWS ElastiCache / Redis OSS Serverless)**
- **Frontend:** **React + React-Bootstrap** dashboard
- **Hosting:** Backend via AWS API Gateway, Frontend on **Netlify**

---

## 🌐 Live Demo

- 🖥 **Dashboard (Frontend):**  
   https://user-creation-app.netlify.app/

- ⚙️ **API Base URL (Backend):**  
   `https://owf5o8rlm8.execute-api.ap-south-1.amazonaws.com/dev`

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

##  Project Structure

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
---

## System Architecture

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

## 🧪 How to Run Locally (Optional)

### Backend (Flask Local)

cd flask-lambda-redis-api
pip install -r requirements.txt

# Start local Redis or update REDIS_HOST in app.py
python app.py

API will run at:
👉 http://localhost:5000

# Frontend (React Local)
cd user-account-dashboard
npm install
npm start


App will run at:
👉 http://localhost:3000

# Api endpoints
| Method | Endpoint       | Description   |
| ------ | -------------- | ------------- |
| POST   | /users         | Create user   |
| GET    | /users/{email} | Fetch user    |
| GET    | /users         | Get all users |
| PUT    | /users/{email} | Update user   |
| DELETE | /users/{email} | Delete user   |

## 🧰 Technology Stack

### Backend
- Python  
- Flask  
- AWS Lambda  
- API Gateway  
- Serverless Framework  
- Redis (ElastiCache Serverless)

### Frontend
- React.js  
- React-Bootstrap  
- Axios  
- Netlify Hosting

---

## 📈 Achievements

✔ Fully serverless architecture  
✔ Live production deployment  
✔ Secure Redis integration  
✔ Responsive dashboard UI  
✔ Scalable and modular codebase  
✔ Real-world recruitment-level implementation  

---

## 👤 Author

**Vignesh**  
Aspiring Backend Developer  
Final Year B.Tech Student  

Built as part of a recruitment task to demonstrate:

- Backend API development  
- Serverless cloud deployment  
- Database integration  
- Frontend dashboard development  

---

## 📬 Contact

For feedback, improvements, or collaboration:

- GitHub Profile  
- LinkedIn (optional)

---

## ✅ Status

🟢 **Project Complete**  
🟢 **Live**  
🟢 **Production Ready**  

