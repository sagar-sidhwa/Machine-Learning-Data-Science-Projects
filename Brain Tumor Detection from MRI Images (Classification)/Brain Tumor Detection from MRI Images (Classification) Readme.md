# 🧠 Brain Tumor Detection from MRI Images (Classification)

## 📖 Project Description
This project focuses on building machine learning and deep learning models for **brain tumor detection using MRI scans**.  
The primary goal was to classify MRI images into **tumor vs. non-tumor categories** using both **custom CNN architectures** and **transfer learning** techniques.

Brain tumors are one of the most serious health conditions, and early detection through medical imaging can significantly improve treatment outcomes. This project demonstrates how AI can assist radiologists by automating tumor detection.

## 📁 Dataset (Link - https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)
- Source: Kaggle Dataset (`https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset`)
---

## ⚙️ Project Workflow
1. **Data Preprocessing**
   - Resized MRI images for uniform input.
   - Normalized pixel values for faster training convergence.
   - Applied **data augmentation** to overcome limited dataset size.

2. **Exploratory Data Analysis (EDA)**
   - Visualized sample MRI scans.
   - Checked class distribution for balance/imbalance.

3. **Model Building**
   - Built a **baseline CNN**.
   - Used **transfer learning** with pre-trained models (VGG16, ResNet, EfficientNet).
   - Added dropout and regularization layers to prevent overfitting.

4. **Model Training & Validation**
   - Train/validation/test split applied.
   - Accuracy and loss monitored across epochs.

5. **Evaluation Metrics**
   - Accuracy, Precision, Recall, F1-score.
   - Confusion Matrix to inspect classification errors.
   - ROC-AUC for threshold evaluation.

6. **Hyperparameter Tuning**
   - Tuned batch size, learning rate, and number of layers.
   - Compared tuned models with baseline CNN.

---

## 📊 Results
- **Baseline CNN**: Decent accuracy but prone to overfitting.  
- **Transfer Learning (ResNet, EfficientNet)**: Achieved **>90% accuracy**.  
- **Best Model**: EfficientNet with tuned parameters showed the most balanced performance across metrics.  

---

## ✅ Conclusion
- Deep Learning models can **accurately classify brain tumors from MRI scans**.  
- Transfer learning significantly improved accuracy compared to a custom CNN.  
- Data augmentation + regularization improved generalization.  
- Future work: use larger datasets, apply ensemble learning, and deploy the model in a real-world diagnostic system.

---

## 🚀 Tech Stack
- **Languages/Libraries**: Python, TensorFlow/Keras, NumPy, Pandas, Scikit-learn, Matplotlib, Seaborn  
- **Techniques**: CNN, Transfer Learning, Data Augmentation, Hyperparameter Tuning  

---

## 🌟 Future Scope
- Train on larger & more diverse MRI datasets.  
- Apply **ensemble CNNs** for improved performance.  
- Deploy as a **web-based diagnostic tool** to assist radiologists.  

---

## 👨‍💻 Author

[Sagar Sidhwa] - 
ML / AI Engineer
MS in CS — AI Track  From Binghamton University 
Focusing ML, and end-to-end real-world projects 
Open to collaboration!


