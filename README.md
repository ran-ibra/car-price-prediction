# 🚗 Car Price Prediction - Kaggle Competition
Kaggle comp. building a model to get the best accuarcy using pipline

This repository contains my solution for the [Car Price Prediction](https://www.kaggle.com/competitions/car-price-prediction-khazani-ahmed) Kaggle competition by Khazani Ahmed.

## 📊 Objective

Predict the **price of a car** based on various features like engine size, fuel type, body type, and more. The evaluation metric is **Root Mean Squared Error (RMSE)**.

---

## 🛠️ What I Did

- 📌 **Data Cleaning & Preprocessing**:
  - Dropped irrelevant features (`CarName`, `carbody`, `enginelocation`, etc.)
  - Handled missing values using mean (numerical) and most frequent (categorical)
  - Mapped categorical strings to numbers (e.g., `doornumber`, `cylindernumber`)

- 🧪 **Feature Engineering**:
  - Encoded categorical variables using OneHotEncoding
  - Scaled numerical variables using StandardScaler
  - Used `FunctionTransformer` to apply custom mappings

- 🔁 **Modeling Pipeline**:
  - Built a reusable pipeline using `Pipeline` and `ColumnTransformer`
  - Trained multiple models including:
    - ✅ Linear Regression
    - ✅ Ridge Regression
    - ✅ (Optional) Random Forest Regressor
  - Tried **log-transformation on the target variable (price)** to reduce skewness

- 🔍 **Evaluation**:
  - Used `train_test_split` for offline validation
  - Evaluated using:
    - R² Score
    - MAE (Mean Absolute Error)
    - RMSE (Root Mean Squared Error)

- 📦 **Submission**:
  - Generated predictions on test data
  - Formatted submission file to include `car_ID` and predicted `price`

---
