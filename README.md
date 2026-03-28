**Credit Card Fraud Detection System using Random Forest**

**Project Overview**
This project focuses on detecting fraudulent credit card transactions using Machine Learning techniques, specifically the **Random Forest Classifier**. 

The system analyzes transaction patterns and classifies them as:
- Legitimate Transaction (0)
- Fraudulent Transaction (1)

Due to the highly imbalanced nature of real-world fraud data, this project also implements multiple resampling techniques such as **Undersampling, Oversampling, and SMOTE**.

**Dataset**

This project uses the **Credit Card Fraud Detection Dataset** from Kaggle:

🔗 Dataset Link:  
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

**Dataset Description**
- Total Transactions: **284,807**
- Fraud Cases: **492**
- Fraud Percentage: **~0.172%**
- Features: **30 numerical features**
  - V1–V28 → PCA transformed features
  - Time → Transaction time
  - Amount → Transaction amount
- Target Variable:
  - `Class = 0` → Normal
  - `Class = 1` → Fraud

The dataset is highly imbalanced, making fraud detection a challenging classification problem. :contentReference[oaicite:1]{index=1}  

**Objectives**

- Detect fraudulent transactions accurately
- Handle class imbalance effectively
- Compare different resampling techniques
- Evaluate model performance using appropriate metrics

**Technologies Used**

- Python 
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Imbalanced-learn (SMOTE)

**Project Workflow**

Data Collection
↓
Data Preprocessing
↓
Exploratory Data Analysis (EDA)
↓
Handling Class Imbalance
↓
Model Training (Random Forest)
↓
Model Evaluation
↓
Feature Importance Analysis

**Data Preprocessing Steps**

- Removed unnecessary feature (`Time`)
- Scaled `Amount` feature using StandardScaler
- Checked missing values
- Split dataset into features and target
- Applied resampling techniques:
  - Undersampling
  - Oversampling
  - SMOTE
  
**Model Used**

**Random Forest Classifier**

- Ensemble learning method
- Combines multiple decision trees
- Reduces overfitting
- Handles non-linear data effectively

**Evaluation Metrics**

Since the dataset is imbalanced, the following metrics were used:

- Precision
- Recall (Very Important ⚠️)
- F1-Score
- Confusion Matrix
- ROC-AUC Score

Accuracy alone is not reliable for imbalanced datasets.

**Results**

- Random Forest performed well across all datasets
- SMOTE provided the best balance between:
  - Fraud detection (Recall)
  - False positives (Precision)
- Achieved high ROC-AUC score indicating strong performance

**Key Insights**

- Fraud transactions are extremely rare (~0.17%)
- Class imbalance significantly affects model performance
- SMOTE improves detection without losing important data
- Feature importance helps identify fraud patterns

**Future Improvements**

- Implement XGBoost / Deep Learning models
- Real-time fraud detection system
- Deploy using Flask or Streamlit
- Add user interface for predictions

**Conclusion**

This project successfully demonstrates a machine learning approach to detecting credit card fraud. By applying Random Forest along with resampling techniques, the model achieves high performance in identifying fraudulent transactions.

SMOTE proved to be the most effective technique for handling class imbalance, making it suitable for real-world applications.

**Author**

- Zagabathuni Udaya Lakshmi
