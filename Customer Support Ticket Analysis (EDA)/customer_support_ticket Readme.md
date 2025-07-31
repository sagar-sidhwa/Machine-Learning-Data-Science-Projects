# 🎫 Customer Support Ticket Classification — Intent Detection with ML & Embeddings

This project focuses on automatically classifying **customer support tickets** into predefined **intent categories** using NLP techniques, including sentence embeddings and machine learning classifiers.

---

## 🧠 Objective

To build a system that can understand and classify incoming customer support messages by **intent**, improving automation and routing efficiency for support teams.

---

## 📁 Dataset (Link - https://www.kaggle.com/datasets/suraj520/customer-support-ticket-dataset)
- Source: Kaggle (Customer Support Ticket Dataset)
- Size: ~8,500 rows
- Target: `Ticket Type` (Multi-class)


## 📁 Dataset Overview

- **Source**: Internal / Public (custom dataset if applicable)
- **Fields**:
  - `category` — general area of the issue
  - `sub_category` — more detailed type
  - `text` — support ticket message
  - `intent` — target label (what the customer wants)


## 📊 Features Used
- Ticket Description (embedded with SentenceTransformers)
- Ticket Priority, Product, Channel, and Subject (encoded)
- Dropped irrelevant columns (name, email, age, resolution, etc.)

## ⚙️ Methodology
1. Cleaned and preprocessed data
2. Encoded categorical variables
3. Text vectorization via Sentence-BERT
4. Concatenated features into a single input matrix
5. Trained RandomForest, Logistic Regression
6. Evaluated using accuracy and classification metrics

## ⚠️ Observations
- This Project's aim was to focus on EDA and not on Model Building
- Ticket text was too generic for models to differentiate
- Future direction: fine-tune an LLM or use contextual classification methods

## 👨‍💻 Author

[Sagar Sidhwa] - 
ML / AI Engineer
MS in CS — AI Track  From Binghamton University 
Focusing ML, and end-to-end real-world projects 
Open to collaboration!
