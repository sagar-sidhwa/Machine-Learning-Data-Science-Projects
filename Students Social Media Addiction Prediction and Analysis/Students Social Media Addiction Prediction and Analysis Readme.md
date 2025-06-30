# 📚 Predicting Student Social Media Addiction Using ML

This machine learning project explores the relationship between student behaviors and social media addiction levels using supervised regression models.

## 📌 Objective
To build a regression model that predicts a student's **Addicted_Score** based on behavioral, academic, and psychological attributes such as:

- Average daily usage
- Sleep hours
- Mental health score
- Social media conflicts
- Academic performance impact
- Relationship status

## 🧠 Dataset Overview (Link - https://www.kaggle.com/datasets/adilshamim8/social-media-addiction-vs-relationships)
- Source: Custom Dataset (Students Social Media Addiction)
- Records: 705
- Target Variable: `Addicted_Score`
- Feature Types:
  - Numerical: Usage hours, Sleep, Mental Health Score, Conflicts
  - Categorical: Gender, Country, Academic Level, Platform

## 🔍 Steps Performed
1. **Data Cleaning**
   - Dropped `Student_ID`
   - Verified no missing values

2. **Exploratory Data Analysis (EDA)**
   - Visualized distribution, outliers, skewness
   - Count plots and boxplots
   - Correlation matrix (after label encoding)

3. **Feature Selection**
   - Random Forest Regressor used for top feature extraction

4. **Feature Engineering**
   - Label & One-Hot Encoding
   - Scaling using StandardScaler

5. **Model Building**
   - Linear Regression
   - Support Vector Regression (SVR)
   - Random Forest Regressor

6. **Model Evaluation**
   - Metrics: R² Score, MAE, RMSE
   - Best Model: Random Forest Regressor (R² ≈ 0.98)

7. **Hyperparameter Tuning**
   - GridSearchCV applied to Random Forest
   - Fine-tuned for best depth, estimators, and split conditions

## 📈 Results
- **Random Forest** performed best with:
  - R² Score: ~0.987
  - MAE: ~0.04
  - RMSE: ~0.17
- Feature importance highlighted:
  - Mental Health
  - Usage Hours
  - Sleep Hours

## ✅ Conclusion
This model can help institutions:
- Monitor digital health
- Intervene early for vulnerable students
- Improve academic support services

---

📁 Project Type: Regression  
📦 Libraries Used: scikit-learn, pandas, seaborn, matplotlib  
🎓 Author: Sagar Sidhwa
