# 🏠 Predicting Home Prices in California using Machine Learning

This project demonstrates how to use Python libraries such as **NumPy**, **Pandas**, and **Scikit-learn** in a Jupyter notebook to predict housing prices in California. We explore two approaches:
1. **Standard ML Workflow**
2. **Scikit-learn Pipelines**

---

## 🎯 Objective

To predict the **median house value** in California blocks using 9 input features.

### 🔢 Feature Variables

- `longitude`: Distance from western California
- `latitude`: Distance from northern California
- `housingMedianAge`: Median age of houses in a block
- `totalRooms`: Total rooms in a block
- `totalBedrooms`: Total bedrooms in a block
- `population`: Total population in a block
- `households`: Total households in a block
- `medianIncome`: Median income of households (in tens of thousands USD)
- `oceanProximity`: Categorical proximity to the ocean

### 🎯 Target Variable

- `medianHouseValue`: Median house value for households (in USD)

---

## 🧰 Dependencies

Install required packages before running the notebook:

```python
%pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## 📊 Data Preprocessing

- Handle missing values
- Encode categorical variables (`oceanProximity`)
- Normalize/scale numerical features
- Train/test split

---

## 🔍 Algorithms Used

Both **standard and pipeline-based** approaches explore:

- **Linear Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **Gradient Boosting Regressor**
- **Support Vector Regressor**
- **K-Nearest Neighbors Regressor**

---

## 🔁 Regular ML Workflow

```python
# Step-by-step ML process
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler, OneHotEncoder
from sklearn.compose import ColumnTransformer
from sklearn.ensemble import RandomForestRegressor
from sklearn.metrics import mean_squared_error

# Load and clean data
df = pd.read_csv("housing.csv")
# Preprocess and train/test split
# Train models, predict, evaluate
```

---

## ⚙️ Pipeline-Based Approach

```python
from sklearn.pipeline import Pipeline
from sklearn.compose import ColumnTransformer

# Define numerical and categorical transformations
numeric_transformer = Pipeline(steps=[
    ('scaler', StandardScaler())
])

categorical_transformer = Pipeline(steps=[
    ('onehot', OneHotEncoder(handle_unknown='ignore'))
])

preprocessor = ColumnTransformer(
    transformers=[
        ('num', numeric_transformer, numeric_features),
        ('cat', categorical_transformer, categorical_features)
    ])

# Combine with ML model
model_pipeline = Pipeline(steps=[
    ('preprocessor', preprocessor),
    ('regressor', RandomForestRegressor())
])

# Fit and evaluate
model_pipeline.fit(X_train, y_train)
preds = model_pipeline.predict(X_test)
```

---

## 📈 Evaluation Metrics

- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **R² Score**

---

## 📁 File Structure
```
├── Home_price_list.csv
├── Home_price_pred_Pipeline.ipynb
├── Home_price_prediction.ipynb
└── README.md
```
