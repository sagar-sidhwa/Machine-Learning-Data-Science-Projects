# 💧 Molecular Solubility Prediction using SMILES

This project predicts the aqueous solubility of chemical compounds using their **SMILES representation** and physicochemical features.

## 📌 Objective
To build a regression model that predicts the **logS (aqueous solubility)** of a molecule based on molecular descriptors derived from SMILES strings.

## 🧠 Dataset Overview
- Dataset: `delaney.csv` (based on the Delaney solubility dataset)
- Records: ~1,100 molecules
- Columns: 
  - `smiles`: Simplified molecular-input line-entry system
  - `logS`: Target solubility value
  - Calculated descriptors: Molecular weight, LogP, H-bond acceptors/donors, etc.

## 🔍 Steps Performed
1. **Data Cleaning & Parsing**
   - Parsed `smiles` using RDKit
   - Computed descriptors (e.g., LogP, MolWt)

2. **Feature Engineering**
   - Created new features (e.g., ring count, rotatable bonds)
   - Scaled features with StandardScaler

3. **Model Building**
   - Linear Regression
   - Ridge/Lasso
   - Random Forest Regressor
   - XGBoost Regressor

4. **Model Evaluation**
   - Metrics: R² Score, RMSE, MAE
   - Baseline comparison against null model
   - Visualized prediction vs actual

5. **Hyperparameter Tuning**
   - Applied GridSearchCV on Ridge and Random Forest

## 🧪 Results
- Achieved **R² ≈ 0.85+** with tuned Random Forest
- Strong feature correlations with molecular weight, LogP, and polar surface area

## ✅ Conclusion
- The model is capable of accurately estimating molecular solubility
- Useful for early drug discovery & ADMET screening
- SMILES-based featurization + classical ML remains powerful for chemical regression tasks

---

📁 Project Type: Regression  
🧪 Domain: Cheminformatics  
🛠 Libraries: RDKit, scikit-learn, pandas, matplotlib  
🎓 Author: Sagar Sidhwa
