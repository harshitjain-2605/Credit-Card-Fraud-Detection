# 💳 Credit Card Fraud Detection & Risk Analytics Platform

## 📌 Overview

Developed an end-to-end machine learning fraud detection system using Python, SQL, Scikit-Learn, XGBoost, and SMOTE to identify fraudulent credit card transactions from a dataset containing 284,807 financial transactions.

The project combines exploratory data analysis, SQL-based business analysis, feature engineering, class imbalance handling, predictive modeling, and fraud-risk analytics to support data-driven fraud prevention and customer protection initiatives.

---

## 🎯 Business Problem

Financial institutions process millions of transactions every day. Fraudulent transactions can result in significant financial losses, operational inefficiencies, and reduced customer trust.

Key challenges include:

- Extremely imbalanced transaction data
- High cost of missed fraud cases
- Need for scalable fraud detection systems
- Minimizing false alerts while maximizing fraud identification

The objective of this project was to build a machine learning solution capable of accurately identifying high-risk transactions before financial damage occurs.

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

### Target Variable

| Class | Description |
|---------|---------|
| 0 | Legitimate Transaction |
| 1 | Fraudulent Transaction |

---

## 🛠 Technologies Used

### Programming Languages

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

### Key Findings

- Dataset contained 284,807 transactions and 492 fraudulent transactions.
- Fraudulent transactions represented only 0.17% of all records, making this a highly imbalanced classification problem.
- No missing values were present, ensuring high-quality input data.
- Significant behavioral differences existed between legitimate and fraudulent transactions.
- Severe class imbalance required specialized techniques for effective fraud detection.

### Fraud Distribution

![Fraud Distribution](images/fraud_distribution.png)

---

## 🗄 SQL-Based Business Analysis

SQL was used to perform transaction-level business analysis and identify fraud-related trends.

Example analyses included:

- Fraud transaction counts
- Average fraudulent transaction amount
- High-value fraud transaction identification
- Transaction pattern exploration

Example Query:

```sql
SELECT AVG(Amount)
FROM transactions
WHERE Class = 1;
```

---

## ⚙ Methodology

### 1. Data Validation & Quality Checks

- Verified dataset integrity
- Checked for missing values
- Performed exploratory statistical analysis

### 2. Feature Engineering

Created additional features to improve predictive performance:

- Log-transformed transaction amount
- Transaction hour extraction
- Behavioral transaction indicators

### 3. Handling Class Imbalance

Implemented SMOTE (Synthetic Minority Oversampling Technique) to address severe class imbalance and improve minority-class detection.

### 4. Model Development

Developed and evaluated multiple machine learning models:

- Logistic Regression
- Random Forest
- XGBoost

### 5. Model Evaluation

Models were assessed using:

- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix

Special emphasis was placed on **Recall**, as undetected fraudulent transactions represent the highest business risk.

---

## 📈 Results

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|---------|---------|---------|---------|---------|---------|
| Logistic Regression | 97.43% | 5.81% | 91.84% | 10.94% | 97.22% |
| Random Forest | 99.95% | 87.10% | 82.65% | 84.82% | 98.12% |
| XGBoost | 99.85% | 54.84% | 86.73% | 67.19% | 97.89% |

### Performance Analysis

- Logistic Regression achieved the highest Recall (91.84%) but generated excessive false positives.
- Random Forest delivered the strongest balance between Precision and Recall.
- XGBoost achieved competitive performance but lower precision than Random Forest.
- Random Forest was selected as the final production model due to its superior overall fraud-detection capability.

---

## 🏆 Key Results

- Processed and analyzed **284,807 financial transactions**.
- Detected fraud within a dataset containing only **0.17% fraudulent records**.
- Applied **SMOTE** to improve minority-class identification.
- Evaluated Logistic Regression, Random Forest, and XGBoost models.
- Achieved:
  - **99.95% Accuracy**
  - **87.10% Precision**
  - **82.65% Recall**
  - **84.82% F1 Score**
  - **98.12% ROC-AUC**
- Selected Random Forest as the final model due to its strong balance between fraud detection effectiveness and false-positive control.

---

## 📊 Model Visualizations

### Confusion Matrix

![Confusion Matrix](images/confusion_matrix.png)

### ROC Curve

![ROC Curve](images/roc_curve.png)

### Feature Importance

![Feature Importance](images/feature_importance.png)

---

## 💡 Business Impact

This solution demonstrates how machine learning can support fraud prevention initiatives in financial institutions by:

- Improving identification of potentially fraudulent transactions
- Reducing financial risk exposure
- Supporting data-driven decision making
- Enhancing customer protection strategies
- Enabling scalable transaction monitoring systems

The final model provides strong predictive performance while maintaining practical business usability for fraud investigation workflows.

---

## 🚀 Interactive Dashboard

An interactive Streamlit application was developed to enable real-time fraud risk assessment and transaction analytics.

### Features

- Fraud probability prediction
- Transaction risk classification
- Interactive analytics dashboard
- Real-time user input support
- Model-based fraud scoring

### Live Demo

🔗 Add your deployed Streamlit link here

---

## 🔮 Future Enhancements

Potential improvements include:

- Real-time transaction streaming pipelines
- Explainable AI using SHAP values
- Deep learning-based fraud detection
- Automated fraud alert generation
- Cloud deployment on AWS/Azure/GCP
- Transaction anomaly detection systems

---

## 👨‍💻 Author

**Harshit Jain**

Computer Engineering Student  
Thapar Institute of Engineering & Technology

LinkedIn: https://linkedin.com/in/your-profile

GitHub: https://github.com/harshitjain-2605

---

## ⭐ Skills Demonstrated

- Machine Learning
- Fraud Detection
- Data Analytics
- SQL Analysis
- Data Quality Management
- Feature Engineering
- Risk Analytics
- Model Evaluation
- Data Visualization
- Business Problem Solving
- Predictive Modeling
- End-to-End Data Science Workflow
