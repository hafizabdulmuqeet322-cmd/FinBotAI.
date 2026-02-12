# 🚀 How to Run FinBot AI

Your Web Application is ready! Here are the steps to run and access it.

## 1. Start the Backend (API & AI)
Open a terminal in the project folder (`d:\FinBotAI`) and run:
```bash
uvicorn backend.main:app --reload --port 8001
```
*Wait until you see: `Application startup complete.`*

## 2. Start the Frontend (Web Interface)
Open a **new** terminal in the frontend folder (`d:\FinBotAI\frontend`) and run:
```bash
npm run dev
```
*Wait until you see: `Local: http://localhost:5173/`*

## 3. Access the App
Open your browser and visit:
👉 **[http://localhost:5173](http://localhost:5173)**

---

### 🔑 Login Credentials (or Register New)
You can register a new account, or use these existing credentials if you haven't deleted the database:
- **Email:** `test@example.com`
- **Password:** `password123`

### 📚 API Documentation (Backend)
To see the raw AI and data endpoints:
- **[http://127.0.0.1:8001/docs](http://127.0.0.1:8001/docs)**
