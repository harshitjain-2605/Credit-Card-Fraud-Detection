# 💳 Credit Card Fraud Detection & Risk Analytics Platform

## 📌 Overview

Developed an end-to-end Machine Learning solution for detecting fraudulent credit card transactions using transaction-level financial data. The objective was to identify potentially fraudulent transactions with high recall while minimizing false positives, helping financial institutions reduce financial losses and improve customer trust.

The project combines data analytics, SQL-based business analysis, feature engineering, class imbalance handling, and machine learning to build a scalable fraud detection system.

---

## 🎯 Business Problem

Financial institutions process millions of transactions daily. Fraudulent transactions can result in substantial financial losses and negatively impact customer experience.

Key challenges include:

- Extremely imbalanced transaction data
- High cost of missed fraud cases
- Need for accurate risk identification
- Maintaining customer trust while reducing unnecessary fraud alerts

The goal was to develop a predictive model capable of identifying high-risk transactions before financial damage occurs.

---

## 📊 Dataset

**Source:** Kaggle Credit Card Fraud Detection Dataset

### Dataset Characteristics

| Metric | Value |
|----------|----------|
| Total Transactions | 284,807 |
| Fraudulent Transactions | 492 |
| Legitimate Transactions | 284,315 |
| Fraud Rate | 0.172% |
| Features | 30 |

Target Variable:

| Class | Description |
|---------|---------|
| 0 | Legitimate Transaction |
| 1 | Fraudulent Transaction |

---

## 🛠 Technologies Used

### Programming

- Python
- SQL

### Libraries

- Pandas
- NumPy
- Scikit-Learn
- XGBoost
- Imbalanced-Learn (SMOTE)
- Matplotlib
- Seaborn

### Tools

- Jupyter Notebook
- Git
- GitHub
- Streamlit

---

## 🔍 Exploratory Data Analysis

Performed comprehensive exploratory analysis to understand transaction behavior and fraud patterns.

Key observations:

- Fraudulent transactions represented less than 0.2% of all transactions.
- Transaction amounts showed significant variation between legitimate and fraudulent activities.
- Severe class imbalance required specialized handling techniques.
- Time-based transaction patterns revealed useful behavioral insights.

### Fraud Distribution

![Fraud Distribution](images/fraud_distribution.png)

---

## 🗄 SQL-Based Analysis

SQL was used to perform business-oriented transaction analysis and identify fraud-related trends.

Example analyses included:

- Fraud transaction counts
- Average fraudulent transaction amount
- High-value fraud transaction identification
- Transaction pattern exploration

Example query:

```sql
SELECT AVG(Amount)
FROM transactions
WHERE Class = 1;
```

---

## ⚙ Methodology

The project followed a structured machine learning workflow:

### Data Preparation

- Data validation and quality checks
- Missing value verification
- Transaction feature analysis

### Feature Engineering

Created additional features including:

- Log-transformed transaction amount
- Transaction hour extraction
- Behavioral transaction indicators

### Class Imbalance Handling

Implemented SMOTE (Synthetic Minority Oversampling Technique) to balance minority fraud samples and improve fraud detection capability.

### Model Development

Developed and evaluated:

- Logistic Regression
- Random Forest
- XGBoost

### Model Evaluation

Performance was assessed using:

- Precision
- Recall
- F1 Score
- ROC-AUC

Special emphasis was placed on Recall because undetected fraudulent transactions represent the highest business risk.

---

## 📈 Results

| Model | Accuracy | Precision | Recall | F1 Score |
|---------|---------|---------|---------|---------|
| Logistic Regression | XX | XX | XX | XX |
| Random Forest | XX | XX | XX | XX |
| XGBoost | XX | XX | XX | XX |

*(Replace with actual project results.)*

### Confusion Matrix

![Confusion Matrix](images/confusion_matrix.png)

### ROC Curve

![ROC Curve](images/roc_curve.png)

### Feature Importance

![Feature Importance](images/feature_importance.png)

---

## 💡 Business Impact

This solution demonstrates how machine learning can support fraud prevention strategies in financial institutions by:

- Improving identification of potentially fraudulent transactions
- Reducing financial risk exposure
- Supporting data-driven decision making
- Enhancing customer protection initiatives
- Enabling scalable transaction monitoring

---

## 🚀 Interactive Dashboard

An interactive Streamlit application was developed to enable real-time fraud risk assessment and transaction analytics visualization.

Features include:

- Transaction risk prediction
- Fraud probability estimation
- Interactive analytics dashboard
- Real-time user inputs

Live Demo:

[Add Streamlit Deployment Link]

---

## 🔮 Future Enhancements

Potential future improvements include:

- Real-time transaction streaming
- Explainable AI using SHAP values
- Deep learning-based fraud detection
- Automated fraud alert generation
- Cloud-native deployment architecture

---

## 👨‍💻 Author

**Harshit Jain**

Computer Engineering Student  
Thapar Institute of Engineering & Technology

LinkedIn: [Your LinkedIn Profile]

GitHub: [Your GitHub Profile]
