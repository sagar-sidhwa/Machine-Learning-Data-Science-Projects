# 🏦 Bank IT Support Ticket Classification — Predicting Customer Intent

This project classifies **customer support tickets** in a banking domain into predefined **intent categories** using sentence embeddings and traditional machine learning models.

---

## 🧠 Objective

To predict the **intent** behind a customer’s support ticket by analyzing the textual description of the issue, enabling faster routing and resolution in a bank's IT support system.

---

## 📁 Dataset (Link - https://huggingface.co/datasets/rbojja/labelled_bank_support_dataset)
- Source: HuggingFace Dataset Hub (`rbojja/labelled_bank_support_dataset`)
- Fields: `domain`, `subdomain`, `category`, `example`, `intent`

## 📁 Dataset Overview

- **Source**: HuggingFace Dataset Hub  
  → [`rbojja/labelled_bank_support_dataset`](https://huggingface.co/datasets/rbojja/labelled_bank_support_dataset)
- **Fields**:
  - `domain`
  - `subdomain`
  - `category`
  - `example` (text)
  - `intent` (target label)

---

## 🧱 Project Steps

### 1. 📦 Data Cleaning & Preprocessing
- Removed low-frequency intent classes (appearing <2 times)
- Cleaned text data, ensured type consistency

### 2. 🔤 Embedding Generation
- Used **`sentence-transformers`** (`all-MiniLM-L6-v2`) to convert support text into numerical vectors (dense embeddings)

### 3. 🤖 Model Building
Trained and evaluated the following classifiers on the embeddings:
- Logistic Regression
- SGD Classifier
- Random Forest
- MLP Classifier

### 4. 🔧 Hyperparameter Tuning
- Used `GridSearchCV` for model selection and tuning
- Applied **Stochastic Gradient Descent (SGD)** where applicable (e.g., in SGDClassifier, MLP, and Logistic Regression with `solver='saga'`)

---

## 🧪 Evaluation Metrics

Evaluated using:
- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**
- Nearest Neighbors lookup for qualitative inspection (KNN)

---

## 📊 Results Snapshot

| Model              | Notes                                      |
|-------------------|---------------------------------------------|
| Logistic Regression | Balanced performance with `saga` solver  |
| SGD Classifier     | Fast, tunable, worked well with embeddings |
| Random Forest      | Captured non-linear patterns               |
| MLP Classifier     | SGD used as optimizer, moderate accuracy   |

> ⚠️ Model performance was limited by **intent overlap** and **possible label noise** in the dataset.

---

## 📌 Tech Stack

- **Language**: Python  
- **Libraries**:  
  - `sentence-transformers` for embeddings  
  - `scikit-learn` for modeling and tuning  
  - `pandas`, `numpy` for data handling  
  - `matplotlib`, `seaborn` for visualization  

---

## 🚀 Future Work

- Add few-shot LLM-based intent classification (OpenAI or Cohere)
- Explore clustering for semi-supervised intent discovery
- Improve preprocessing for synonyms and phrase grouping
- Introduce explainability (e.g., SHAP for feature importance)

---

## 🔧 Technologies Used
- Python
- SentenceTransformers
- Scikit-learn
- Pandas, NumPy, Seaborn

## ⚙️ Methodology
1. Extract embeddings using `sentence-transformers`
2. Apply classifiers: Logistic Regression, Random Forest
3. Evaluate with accuracy, precision, recall, F1-score

## ✅ Outcome
Achieved moderate classification accuracy due to potential label noise and intent overlaps.

---

## 👨‍💻 Author

[Sagar Sidhwa] - 
ML / AI Engineer
MS in CS — AI Track  From Binghamton University 
Focusing ML, and end-to-end real-world projects 
Open to collaboration!
