# 🤖 FinBot AI: The Intelligent Financial Operating System

FinBot AI is a next-generation personal finance assistant that goes beyond simple tracking. It uses **predictive AI**, **real-time currency conversion**, and **gamification** to help you master your financial life.

![FinBot AI Dashboard](https://via.placeholder.com/800x400.png?text=FinBot+AI+Dashboard+Preview)

## 🌟 Key Features

### 🧠 Advanced AI & Intelligence
-   **Predictive Analytics**: Forecasts next month’s spending with ~89% accuracy using Random Forest Regression.
-   **Smart Categorization**: Automatically categorizes transactions based on descriptions (e.g., "Uber" -> Transport).
-   **Financial Health Score**: A live 0-100 score assessing your financial stability based on income, spending, and savings.
-   **RAG Chatbot**: A "Digital Financial Advisor" that knows your specific financial context and gives tailored advice.

### 🌍 Global & Multi-Currency
-   **Real-Time Conversion**: Supports **USD, EUR, GBP, INR, PKR, JPY**.
-   **Unified View**: See your total net worth in your preferred base currency, regardless of transaction origin.
-   **Currency Fluctuation**: Simulated live market rates for realistic international financial management.

### 🎮 Gamification & Engagement
-   **Badges & Trophies**: Earn awards for hitting savings goals (e.g., "Saver Badge", "Goal Crusher").
-   **Savings Streak**: Track consecutive days of staying within budget.
-   **Community Leaderboard**: Compare your "Financial XP" with other (AI-simulated) users.

### 🔒 Security & Privacy
-   **Local-First Architecture**: Your data stays private.
-   **Account Deletion**: Full "Right to be Forgotten" with a single click.

---

## 🛠️ Tech Stack

### Frontend
-   **React 18** (Vite)
-   **Tailwind CSS v4** (Modern Styling)
-   **Recharts** (Interactive Data Viz)
-   **Lucide React** (Beautiful Icons)

### Backend
-   **FastAPI** (High-performance Python API)
-   **SQLAlchemy** (ORM & Database Management)
-   **Scikit-Learn** (Machine Learning Core)
-   **Google Gemini API** (LLM Chatbot Intelligence - Optional)
-   **SQLite** (Development Database)

---

## 🚀 Getting Started

### Prerequisites
-   Node.js (v16+)
-   Python (v3.9+)

### 1️⃣ Backend Setup
```bash
cd backend
# Create virtual environment
python -m venv venv
# Activate (Windows)
venv\Scripts\activate
# Install dependencies
pip install -r requirements.txt
# Run Server
python -m uvicorn main:app --reload
```
*Server runs at `http://localhost:8000`*

### 2️⃣ Frontend Setup
```bash
cd frontend
# Install dependencies
npm install
# Run Development Server
npm run dev
```
*App runs at `http://localhost:5173`*

---

## 🔑 Environment Variables
Create a `.env` file in the `backend` directory:
```env
GOOGLE_API_KEY=your_gemini_api_key_here
SECRET_KEY=your_jwt_secret_key
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30
```

---

## 📚 API Documentation
Once the backend is running, visit:
**[http://localhost:8000/docs](http://localhost:8000/docs)**
for interactive Swagger UI documentation.

---

## 🤝 Contributing
1.  Fork the repo
2.  Create your feature branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

---

## 📄 License
Distributed under the MIT License. See `LICENSE` for more information.
