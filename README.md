# 🏡 Home Price Prediction — ML Hands-On

Welcome to the `ml-hands-on` repository! This project is a practical implementation of machine learning workflows to predict house prices. It covers raw data processing, training regression models, creating pipelines, and exploring improved techniques.

---

## 📁 Repository Structure

```
ml-hands-on/
├── Home_price_list.csv                     # Dataset for basic models
├── Home_price_prediction.ipynb             # Basic Linear Regression notebook
├── Home_price_pred_Pipeline.ipynb          # ML pipeline-based version
└── new_approach/
    ├── Housing.csv                         # Alternate dataset
    └── housing_pred_cal_ml.ipynb           # Newer approach with deeper feature engineering
```

---


## 📌 Project Objectives

- Build regression models to predict housing prices
- Use Scikit-learn for modeling and preprocessing
- Apply pipelines for clean, reproducible code
- Experiment with different datasets and techniques

---

## 📊 Datasets

### 🏘️ `Home_price_list.csv`

Basic dataset with features like:
- Area
- Number of bedrooms
- Price

### 🏡 `Housing.csv`

Found in `new_approach/`, includes:
- Advanced features
- More room for experimentation

---

## 🧠 Notebooks Summary

### 📘 `Home_price_prediction.ipynb`

- Loads and explores dataset
- Trains a simple Linear Regression model
- Visualizes results

### 📗 `Home_price_pred_Pipeline.ipynb`

- Introduces `Pipeline` and `ColumnTransformer`
- Handles preprocessing and modeling together
- More robust and production-friendly

### 📙 `housing_pred_cal_ml.ipynb`

- Uses the dataset in `new_approach/Housing.csv`
- Adds feature engineering
- Prepares a better, more scalable solution

---
