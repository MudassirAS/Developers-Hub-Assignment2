# 🏦 Term Deposit Subscription Prediction (Bank Marketing)

## 📌 Overview
This project is part of my Data Science & AI/ML internship at **DevelopersHub Corporation**.  
The objective is to predict whether a bank customer will subscribe to a **term deposit** as a result of a marketing campaign.  

The task involves:
- Data preprocessing and feature encoding  
- Classification model building (Logistic Regression & Random Forest)  
- Model evaluation with Confusion Matrix, F1-Score, and ROC Curve  
- Model interpretability using **SHAP** (Explainable AI)  
- Business insights from predictions  

---

## 📂 Dataset
The dataset is the **Bank Marketing Dataset** from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/bank+marketing).  

- **Rows**: 45,211  
- **Features**: 16 (client info, campaign details, etc.)  
- **Target**: `y` (whether the client subscribed to a term deposit: yes/no)  

---

## ⚙️ Methodology
1. **Data Preprocessing**  
   - Encoded categorical variables using One-Hot Encoding  
   - Scaled numeric features for Logistic Regression  
   - Handled target imbalance in evaluation  

2. **Modeling**  
   - Logistic Regression (baseline model)  
   - Random Forest (non-linear ensemble model)  

3. **Evaluation Metrics**  
   - Confusion Matrix  
   - Precision, Recall, F1-score  
   - ROC Curve & AUC  

4. **Explainability**  
   - Used **SHAP values** to interpret model predictions  
   - Explained 5 random predictions to understand feature importance  

---

## 📊 Results

### 🔹 Logistic Regression
          precision    recall  f1-score   support

       0       0.92      0.97      0.95      7985
       1       0.64      0.35      0.45      1058

accuracy                           0.90      9043
macro avg      0.78      0.66      0.70      9043
weighted avg   0.89      0.90      0.89      9043



### 🔹 Random Forest
              precision    recall  f1-score   support

           0       0.93      0.97      0.95      7985
           1       0.67      0.41      0.51      1058

accuracy                               0.91      9043
macro avg          0.80      0.69      0.73      9043
weighted avg       0.90      0.91      0.90      9043


---

## 📈 Insights
- Both models perform well in predicting **non-subscribers (class 0)** but struggle with **subscribers (class 1)** due to class imbalance.  
- **Random Forest** slightly outperforms Logistic Regression in recall for subscribers.  
- **Key Influential Features (from SHAP analysis):**
  - Contact method (`cellular` improves likelihood of success)  
  - Duration of last call  
  - Client balance and age  
  - Campaign frequency (too many contacts reduce success rate)  

---

## ✅ Conclusion
- Random Forest is the preferred model with **higher recall for positive class**.  
- SHAP interpretability shows that **marketing strategy should focus on high-balance clients, with targeted and timely contact methods**.  
- For better results, future work could include:
  - Handling class imbalance using **SMOTE or class weighting**  
  - Trying advanced models like **XGBoost**  

---

## 🛠️ Tools & Libraries
- Python, Pandas, NumPy  
- Scikit-learn, Random Forest, Logistic Regression  
- Matplotlib, Seaborn (visualizations)  
- SHAP (Explainable AI)  

---
