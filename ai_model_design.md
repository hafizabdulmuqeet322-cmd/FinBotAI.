# AI Model Design & Pipeline

## 1. AI Pipeline Overview
The AI module is designed to perform two distinct tasks: **Regression** (Spending Prediction) and **Classification** (Behavior Analysis).

```mermaid
flowchart LR
    RawData[Raw Transaction Data] --> Preprocess[Preprocessing & Feature Engineering]
    Preprocess --> Split{Train/Test Split}
    
    Split --> TrainReg[Train Regressor (RandomForest)]
    Split --> TrainCls[Train Classifier (RandomForest)]
    
    TrainReg --> ModelReg[[spending_model.pkl]]
    TrainCls --> ModelCls[[behavior_model.pkl]]
    
    ModelReg --> Inference
    ModelCls --> Inference
    
    Input[User History] --> Inference[Real-time Prediction]
    Inference --> Output[Forecast & Behavior Label]
```

## 2. Model Details

### A. Spending Predictor
- **Goal**: Predict total spending for the next month.
- **Algorithm**: `RandomForestRegressor`
    - Chosen for its ability to handle non-linear relationships and resistance to overfitting compared to simple linear models.
- **Features**:
    - `month`: Seasonality factor.
    - `year`: Trend factor.
    - `category_encoded`: Impact of specific categories.
    - `lag_1_month`: Spending from the previous month (Contextual).

### B. Behavior Classifier
- **Goal**: Categorize user financial health.
- **Algorithm**: `RandomForestClassifier`
- **Classes**:
    - `Saver`: High savings rate (>20%).
    - `Spender`: High discretionary spending.
    - `Risky`: Expenses > Income.
    - `Balanced`: Moderate spending and savings.
- **Features**:
    - `income_expense_ratio`
    - `savings_rate`
    - `discretionary_percentage`

## 3. Data Processing
- **Normalization**: Standard scaling applied to monetary values.
- **Encoding**: Label encoding for categorical variables (e.g., 'Food', 'Rent').
- **Handling Missing Data**: Mean imputation (though synthetic data is clean).

## 4. Performance Metrics
- **Regression**: R² Score (Target > 0.85), MAE (Mean Absolute Error).
- **Classification**: Accuracy, Precision, Recall matrix.
