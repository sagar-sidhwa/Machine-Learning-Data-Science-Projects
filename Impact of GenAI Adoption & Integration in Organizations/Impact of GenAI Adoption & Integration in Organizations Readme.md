# 📊 Impact of GenAI Adoption & Integration in Organizations Productivity

This machine learning project predicts the **Productivity Change (%)** after adopting **Generative AI** in large enterprises using structured and unstructured data.

## 🧠 Problem Statement
With the rise of GenAI adoption, companies are observing varied levels of impact on workforce productivity. This project aims to predict how much productivity is affected based on company attributes, tools used, employee sentiment, and training hours.

## 🔍 Dataset (Link - https://www.kaggle.com/datasets/tfisthis/enterprise-genai-adoption-and-workforce-impact-data)
- Source: Kaggle
- Records: 100,000
- Features:
  - `Company Name`, `Industry`, `Country`, `GenAI Tool`, `Employee Sentiment` (Categorical)
  - `Adoption Year`, `Training Hours`, `New Roles`, `Employees Impacted` (Numerical)
- Target: `Productivity Change (%)`

## 📦 Techniques Used
- **Text Processing:** TF-IDF and LLM Embeddings
- **Encoding:** One-Hot Encoding & Standard Scaling
- **Regression Models:**
  - Linear Regression
  - Ridge Regression (Tuned)
  - Random Forest Regressor
  - XGBoost Regressor
  - LightGBM Regressor
- **Model Evaluation:** R² Score, RMSE
- **Hyperparameter Tuning:** GridSearchCV
- **Cross Validation:** 5-fold

## ❗ Observations
- Many models, even after tuning, achieved **very low R² scores**
- Tree-based models performed slightly better
- LLM-based embeddings did not significantly outperform TF-IDF
- **Possible issues:**
  - Features have weak correlation with target
  - Target (`Productivity Change (%)`) may be noisy or inconsistent
  - True influencing factors may not be in dataset

## ✅ Conclusion
This project highlights challenges in modeling business productivity where the relationship between features and outcome is complex and non-linear. It showcases strong ML pipeline practice and critical thinking in evaluating model limitations.

## 📌 Future Work
- To Investigate external factors and improve feature engineering.
- Considering transforming the target variable for better performance.
- Explore alternative modeling techniques.

---

🛠 Built with Scikit-Learn, XGBoost, LightGBM  
🎓 Author: Sagar Sidhwa  
📁 Project Repo: [Machine-Learning-Data-Science-Projects][https://github.com/sagar-sidhwa/Machine-Learning-Data-Science-Projects]
