# 💼 Machine Learning Job Postings in the US — Predicting Seniority Level

This project aims to predict the **seniority level** of job postings based on various job-related metadata and descriptions using traditional NLP (TF-IDF) and modern LLM-based embeddings (BERT).

---

## 🧠 Objective

To classify the **seniority level** (Entry-level, Mid-Senior, Executive, etc.) of machine learning job postings in the US based on:
- Job title & description
- Company information
- Location & days since posting

---

## 📁 Dataset Overview

- Source: Kaggle
- Records: ~988 job postings
- Columns include:
  - `job_description_text`, `company_description`
  - `company_name`, `company_address_locality/region`
  - `job_title`, `seniority_level` (target)

---

## 🧱 Project Steps

### 1. 📦 Data Cleaning & Preprocessing
- Dropped unnecessary columns (e.g., raw date, website)
- Engineered `days_since_posted` feature from date
- Handled missing values using indicators

### 2. ✍️ Feature Engineering
- Combined textual columns into a single `full_text`
- Applied `TF-IDF` for text vectorization
- Categorical features were One-Hot Encoded via `ColumnTransformer`

### 3. 🤖 Model Building (TF-IDF Pipeline)
Trained and evaluated the following classifiers:
- Logistic Regression
- Random Forest
- SVM
- XGBoost
- LightGBM

Included:
- Accuracy
- Cross-validation scores
- Hyperparameter tuning using `GridSearchCV`

### 4. 🔤 LLM Embedding Pipeline (Sentence-BERT)
- Replaced TF-IDF with LLM embeddings using `sentence-transformers`
- Used `X_train_embeddings` and combined structured features
- Re-evaluated models using same setup for comparison

---

## 🔍 Results & Insights

| Model              | TF-IDF Accuracy | LLM Accuracy |
|-------------------|-----------------|--------------|
| Logistic Regression | ~64~%            | Slightly better |
| Random Forest       | ~62~%            | Improved slightly |
| XGBoost             | ✅ Best @ TF-IDF | Good           |
| LightGBM            | Decent          | Decent         |

> ⚠️ Note: Results are modest due to **small dataset size (~988)** and missing values. LLM embeddings improved slightly but are limited without enough data.

---

## 🎯 Conclusion

- TF-IDF still performs well for smaller datasets
- LLMs can help with richer representations but need more data
- Structured + unstructured feature blending is essential
- Avoid overfitting — a model achieving 100% accuracy is **not realistic**

---

## 📌 Tech Stack

- Python, Pandas, Scikit-learn
- TF-IDF Vectorizer, SentenceTransformers
- Logistic Regression, RandomForest, SVM, XGBoost, LightGBM
- Cross-validation, GridSearchCV
- Matplotlib & Seaborn for EDA

---

## 📚 Future Improvements

- Increase dataset size
- Use advanced LLMs like OpenAI or Cohere embeddings
- Try ensemble or stacking classifiers
- Add explainability (e.g., SHAP, LIME)

---

## 👨‍💻 Author

Sagar Sidhwa  
Pursuing MS in CS — AI Track  
Focusing on NLP, ML, and end-to-end real-world projects
