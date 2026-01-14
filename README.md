# 🛒 Walmart Sales Prediction Using XGBoost

This project leverages machine learning to predict whether a given business week includes a holiday using the Walmart Sales Dataset. By analyzing factors like environmental conditions and economic indicators, the model classifies the `Holiday_Flag` (0 or 1).

---

## 📊 Project Overview

Holiday weeks in retail significantly affect logistics and consumer behavior. This project uses **XGBoost**, a powerful gradient boosting algorithm, to predict holiday weeks by analyzing key metrics across 6,435 observations.

**Dataset Features:**
- **Store:** Store identification number
- **Weekly_Sales:** Sales for the given store
- **Temperature:** Average temperature in the region
- **Fuel_Price:** Cost of fuel in the region
- **CPI:** Consumer Price Index
- **Unemployment:** Local unemployment rate

---

## 🛠️ Technical Implementation

The project follows a standard machine learning workflow:

1. **Data Preprocessing**
   - Removing non-numeric columns like `Date`
   - Encoding the target variable `Holiday_Flag` using `LabelEncoder`

2. **Model Training**
   - Implementing the `XGBClassifier` from the XGBoost library

3. **Hyperparameter Analysis**
   - Testing different numbers of estimators (`n_estimators`) to find the optimal balance between performance and computation

---

## 📈 Model Evaluation

The model's performance was measured by its **classification error** across different numbers of trees. The error decreased as more trees were added:

| Number of Trees (`n_estimators`) | Classification Error |
|---------------------------------|--------------------|
| 15                              | 7.30%              |
| 50                              | 6.99%              |
| 100                             | 6.94%              |
| 200                             | 6.42%              |
| 400                             | 5.07%              |
