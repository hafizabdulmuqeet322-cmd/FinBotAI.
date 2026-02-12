# System Architecture & Data Flow

## 1. System Architecture
The application follows a client-server architecture with a clear separation of concerns.

```mermaid
graph TD
    Client[React Frontend] -->|HTTP/JSON| API[FastAPI Backend]
    API -->|ORM| DB[(SQLite Database)]
    API -->|Inference| AI[AI Engine (Scikit-Learn)]
    AI -->|Load| Model[[Trained Models (.pkl)]]
    
    subgraph Backend
    API
    DB
    AI
    Model
    end
    
    subgraph Frontend
    Client
    end
```

## 2. Data Flow Diagram
How data moves from the user to the database and AI components.

```mermaid
sequenceDiagram
    participant User
    participant UI as Frontend (React)
    participant API as Backend (FastAPI)
    participant DB as Database
    participant AI as AI Engine

    User->>UI: Input Expense (Amount, Category)
    UI->>API: POST /expenses/
    API->>DB: Save Expense Record
    DB-->>API: Confirm Save
    API-->>UI: Success Response
    
    User->>UI: View Dashboard
    UI->>API: GET /predict/
    API->>DB: Fetch Recent History
    DB-->>API: Return Data
    API->>AI: Predict(History)
    AI-->>API: Spending Forecast + Behavior Label
    API-->>UI: JSON (Prediction + Recommendation)
    UI->>User: Display Charts & Tips
```
