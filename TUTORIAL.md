# FinBot AI - User Tutorial 📘

Welcome to **FinBot AI**, your intelligent personal finance assistant! This guide will help you navigate the application and make the most of its features.

## 🚀 1. Getting Started

### Access the App
-   **Frontend (Dashboard)**: [http://localhost:5173](http://localhost:5173)
-   **Backend**: [http://127.0.0.1:8001](http://127.0.0.1:8001)

### Login / Register
1.  **Register**: 
    - Click "Register".
    - Enter your email and click **"Send Code"**.
    - **Check the Backend Terminal/Console** for the 6-digit verification code (Mock Email Service).
    - Enter the code, password, and confirm password.
    - Click "Register".
2.  **Login**: Use your credentials to access the dashboard.
3.  **Logout**: Click the "Logout" button in the top-right corner to exit.

> **Note**: Your data is private to your account. Creating a new user will start with a blank dashboard (except for any global dummy data if configured).

---

## 💸 2. Tracking Expenses

Use the **"Add Transaction"** widget on the Dashboard to log your spending.

1.  **Amount**: Enter the value (e.g., `5000`).
2.  **Currency**: Select your currency from the dropdown. separation
    -   Supported: **USD, EUR, GBP, INR, JPY, PKR**.
3.  **Category**: Choose a category (e.g., `Food`, `Tech`).
4.  **Description**: Optional note (e.g., "Dinner with friends").
5.  Click **"Add Transaction"**.

> *Note: The "Total Spending" card will update instantly to reflect this new amount (converted to base currency if applicable).*

---

## 🎯 3. Setting Financial Goals

Track your savings targets with the **"Savings Goals"** widget.

1.  Click **"+ Add Goal"**.
2.  **Name**: E.g., "New Laptop".
3.  **Target Amount**: E.g., `150000`.
4.  **Currency**: Select **PKR** (or others).
5.  Click **"Save Goal"**.
6.  *Progress*: As you save, the progress bar will fill up (future feature: link expenses to goals).

---

## 🤖 4. AI Features

### 🔮 Spending Prediction
-   Look at the **"Predicted (Next Month)"** card.
-   The AI analyzes your past 6 months of data to forecast what you will spend next month.
-   *Tip: Try adding a large expense in the past month via API to see the prediction change!*

### 💡 AI Recommendation
-   The gradient card at the top displays a personalized tip.
-   E.g., *"Your spending on Food is high. Try cooking at home to save ~15%."*

### 💬 Chatbot Assistant
-   Click the **Message Icon** (bottom-right).
-   Ask questions like:
    -   *"How should I save?"*
    -   *"What is the 50/30/20 rule?"*
    -   *"Should I pay off debt?"*

---

## 📊 5. Visualizing Data

-   **Spending Trend**: A line chart showing your expenses over the last 6 months.
-   **Category Breakdown**: A pie chart showing where your money went this month.
-   **Predicted Breakdown**: A bar chart estimating which categories will cost the most next month.

---

## 🛠️ Troubleshooting

-   **"Error connecting to AI"**: Ensure the backend server is running on port 8001.
-   **Data not updating**: Refresh the page.
