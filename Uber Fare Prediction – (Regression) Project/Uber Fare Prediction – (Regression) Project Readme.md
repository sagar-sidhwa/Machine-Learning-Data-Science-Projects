# 🚖 Uber Fare Prediction – Regression Project

## 📌 Overview
This project focuses on predicting **Uber ride fares** using machine learning regression techniques.  
The dataset contains ride-level details like pickup/drop-off locations, datetime, passenger count, and fare amount.  
The goal was to build models that can predict fares accurately and analyze what factors impact them the most.  

## 📁 Dataset (Link - https://www.kaggle.com/datasets/yasserh/uber-fares-dataset)
- Source: Kaggle Dataset (`https://www.kaggle.com/datasets/yasserh/uber-fares-dataset`)
- Data Overview

The dataset consists of 200,000 rows and 9 columns, with the following details:

| Column             | Non-Null Count  | Data Type |
|--------------------|-----------------|-----------|
| **Unnamed: 0**      | 200,000         | int64     |
| **key**             | 200,000         | object    |
| **fare_amount**     | 200,000         | float64   |
| **pickup_datetime** | 200,000         | object    |
| **pickup_longitude**| 200,000         | float64   |
| **pickup_latitude** | 200,000         | float64   |
| **dropoff_longitude**| 199,999        | float64   |
| **dropoff_latitude** | 199,999        | float64   |
| **passenger_count** | 200,000         | int64     |

---

## 🔹 Project Workflow
1. **Data Preprocessing**
   - Handled missing values & outliers
   - Extracted features from datetime (hour, day, month)
   - Engineered trip distance feature

2. **Exploratory Data Analysis (EDA)**
   - Visualized feature distributions
   - Analyzed correlations between predictors and fare amount

3. **Feature Engineering**
   - Created new features
   - Treated skewness in numerical variables

4. **Model Building**
   - Implemented and compared:
     - Linear Regression
     - Ridge Regression
     - Random Forest Regressor
     - XGBoost Regressor
   - Hyperparameter tuning with GridSearchCV

5. **Evaluation**
   - Metrics: RMSE, MAE, R²
   - Feature importance analysis

---

## 📊 Results
- Linear models struggled to capture non-linear patterns.  
- Random Forest & XGBoost achieved the best results with lower errors.  
- **Trip distance** and **time-based features** had the highest impact on predictions.  

---

## 🚀 Future Work
- Experiment with advanced feature engineering (weather, traffic conditions).  
- Try deep learning approaches (LSTMs for time-based features).  
- Deploy the best-performing model as a web API for real-time fare prediction.  


---

## 👨‍💻 Author

[Sagar Sidhwa] - 
ML / AI Engineer
MS in CS — AI Track  From Binghamton University 
Focusing ML, and end-to-end real-world projects 
Open to collaboration!
