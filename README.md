# 🚗 Car Price Prediction (Custom ML Pipeline from Scratch)

This project implements a complete machine learning pipeline from scratch — including data preprocessing, one-hot encoding, feature scaling, gradient descent-based linear regression with optional regularization , categorical variables( one hot encoding) ,Model tuning and performance visualization — all without using ML libraries like `scikit-learn`.

---

## 📂 Dataset

- Source: [ML Bookcamp Car Dataset](https://github.com/alexeygrigorev/mlbookcamp-code/tree/master/chapter-02-car-price)
- Format: CSV
- Target: `msrp` (Manufacturer's Suggested Retail Price)
- Preprocessing: Applied log-transformation on `msrp` for normalization

---

## 📊 Features

### 🔢 Numerical Features:
- `engine_hp`, `engine_cylinders`, `highway_mpg`, `city_mpg`, `popularity`
- Engineered: `age = 2017 - year`

### 🏷️ Categorical Features (Top Categories One-Hot Encoded):
- `make`, `model`, `engine_fuel_type`, `transmission_type`, `driven_wheels`
- `market_category`, `vehicle_size`, `vehicle_style`

### ➕ Engineered Binary Columns:
- Number of doors → `num_doors_2`, `num_doors_3`, `num_doors_4`

---

## ⚙️ ML Pipeline Overview

### 🧹 Preprocessing:
- Cleaned column names, filled missing values
- Log-transformed price
- Standardized numeric features (mean = 0, std = 1)
- One-hot encoded top 5 categories for each categorical column

### 🧠 Model Training:
- Custom gradient descent optimizer
- Optional L2 regularization (Ridge)
- Manual feature scaling and cost computation
- Trained on 60% data, validated on 20%, tested on 20%

### 📈 Evaluation:
- Squared Error: **~0.1249**
- Histogram of predicted vs actual prices
- Residual distribution and scatter plots

---

## 📉 Visualizations

- 📌 Cost vs Iteration
- 📌 Histogram of residuals
- 📌 Residual plot
- 📌 Actual vs Predicted (Scatter)

---



