# 💳 Credit Card Fraud Detection & Risk Analytics Platform

## 📌 Overview

Developed an end-to-end machine learning fraud detection system using Python, SQL, Scikit-Learn, XGBoost, and SMOTE to identify fraudulent credit card transactions from a dataset containing 284,807 financial transactions.

The project combines exploratory data analysis, feature engineering, class imbalance handling, predictive modeling, and fraud-risk analytics to support data-driven fraud prevention and customer protection initiatives.

By evaluating multiple machine learning algorithms and prioritizing fraud detection performance metrics, the project demonstrates how data-driven solutions can be applied to real-world financial risk management problems.

---

## 🎯 Business Problem

Credit card fraud results in significant financial losses for financial institutions and negatively impacts customer trust.

A key challenge in fraud detection is that fraudulent transactions represent only a tiny fraction of all transactions, making the dataset highly imbalanced. Traditional machine learning models often struggle to correctly identify these rare fraud cases.

The objective of this project was to build a predictive fraud detection system capable of accurately identifying fraudulent transactions while minimizing false positives and maximizing fraud detection capability.

---

## 📊 Dataset

**Source:** Kaggle Credit Card Fraud Detection Dataset

### Dataset Characteristics

| Metric | Value |
|----------|----------|
| Total Transactions | 284,807 |
| Fraudulent Transactions | 492 |
| Legitimate Transactions | 284,315 |
| Fraud Rate | 0.1727% |
| Features | 30 Original Features + Engineered Features |
| Target Variable | Class |

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

---

## 🔍 Exploratory Data Analysis

Performed extensive exploratory data analysis to understand transaction behavior and fraud patterns.

### Key Findings

- Dataset contained **284,807 transactions** and **492 fraudulent transactions**.
- Fraudulent transactions represented only **0.1727%** of all transactions.
- No missing values were present in the dataset, ensuring high data quality.
- Transaction behavior exhibited measurable differences between legitimate and fraudulent records.
- Severe class imbalance required specialized techniques for effective fraud detection.

### Fraud Distribution

![Fraud Distribution](images/fraud_distribution.png)

### Transaction Amount Analysis

- Analyzed transaction amount distributions using histograms and boxplots.
- Compared spending behavior across fraudulent and legitimate transactions.
- Applied logarithmic transformation to reduce skewness and improve model learning.

### Time-Based Analysis

- Extracted transaction hour from raw timestamp data.
- Investigated fraud occurrence patterns across different time periods.
- Identified temporal transaction behavior useful for feature engineering.

---

## ⚙ Feature Engineering

To improve predictive performance, additional features were engineered from the raw dataset.

### Feature Engineering Steps

#### Log Amount Transformation

Applied logarithmic transformation to reduce skewness in transaction amounts:

```python
df["LogAmount"] = np.log1p(df["Amount"])
```

Benefits:

- Reduces impact of extreme values
- Improves feature distribution
- Enhances model learning

#### Transaction Hour Extraction

Created a transaction-hour feature:

```python
df["Hour"] = (df["Time"] // 3600).astype(int)
```

Benefits:

- Captures temporal transaction patterns
- Enables time-based fraud analysis
- Improves model interpretability

---

## ⚖ Handling Class Imbalance

One of the most significant challenges in fraud detection is class imbalance.

### Original Distribution

| Class | Count |
|---------|---------|
| Legitimate | 284,315 |
| Fraud | 492 |

To address this issue, **SMOTE (Synthetic Minority Oversampling Technique)** was applied.

### Benefits of SMOTE

- Balances minority-class samples
- Improves fraud detection recall
- Reduces model bias toward majority class
- Enhances classification performance

### Balanced Training Data

| Class | Count |
|---------|---------|
| Legitimate | 227,451 |
| Fraud | 227,451 |

---

## 🤖 Machine Learning Models

Three classification models were trained and evaluated:

### Logistic Regression

Advantages:

- Fast baseline model
- Highly interpretable
- Strong fraud detection recall

### Random Forest

Advantages:

- Robust ensemble model
- Handles nonlinear relationships effectively
- Provides feature importance insights

### XGBoost

Advantages:

- Gradient boosting framework
- Strong predictive capability
- Effective on complex classification tasks

---

## 📈 Model Evaluation

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

### Why Recall Matters

In fraud detection, missing a fraudulent transaction can lead to direct financial loss.

Therefore, Recall was treated as one of the most important evaluation metrics.

---

## 🏆 Model Performance

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|---------|---------|---------|---------|---------|---------|
| Logistic Regression | 97.43% | 5.81% | 91.84% | 10.94% | 97.22% |
| Random Forest | 99.95% | 87.10% | 82.65% | 84.82% | 98.12% |
| XGBoost | 99.85% | 54.84% | 86.73% | 67.19% | 97.89% |

---

## 📊 Performance Analysis

### Logistic Regression

Strengths:

- Highest Recall (91.84%)
- Detected the largest proportion of fraudulent transactions

Limitation:

- Very low Precision (5.81%)
- Generated excessive false positives

---

### Random Forest

Strengths:

- Highest Precision (87.10%)
- Highest F1 Score (84.82%)
- Highest ROC-AUC (98.12%)
- Strong balance between fraud detection and false-positive control

Outcome:

- Selected as the final production model

---

### XGBoost

Strengths:

- Strong Recall (86.73%)
- Competitive ROC-AUC (97.89%)

Limitation:

- Lower Precision than Random Forest

---

## 📊 Visualizations

### Confusion Matrix

<img width="640" height="480" alt="confusion_matrix" src="https://github.com/user-attachments/assets/9377b955-1dbb-4971-8e25-1af5fcffc8d4" />

---

## 💡 Business Impact

This project demonstrates how machine learning can support fraud prevention initiatives in financial institutions by:

- Detecting high-risk transactions with strong predictive performance
- Improving fraud identification capability within highly imbalanced datasets
- Reducing financial risk exposure
- Supporting data-driven decision making
- Enhancing customer protection strategies
- Enabling scalable transaction monitoring systems

The final Random Forest model achieved:

- **99.95% Accuracy**
- **87.10% Precision**
- **82.65% Recall**
- **84.82% F1 Score**
- **98.12% ROC-AUC**

making it highly effective for practical fraud detection scenarios.

---

## 🚀 Key Results

- Processed and analyzed **284,807 credit card transactions**
- Identified fraud within a dataset containing only **0.1727% fraudulent records**
- Applied **SMOTE** to address severe class imbalance
- Engineered additional behavioral features from transaction data
- Evaluated Logistic Regression, Random Forest, and XGBoost models
- Selected Random Forest as the final model due to superior overall performance
- Achieved **98.12% ROC-AUC** and **84.82% F1 Score**
- Demonstrated a complete end-to-end machine learning workflow from data analysis to model evaluation

---

## 🔮 Future Improvements

Potential enhancements include:

- Real-time transaction fraud monitoring
- Explainable AI using SHAP values
- Deep learning-based fraud detection models
- Automated fraud alert generation
- Cloud deployment using AWS or Azure
- Transaction anomaly detection pipelines

---

## 👨‍💻 Author

**Harshit Jain**

Computer Engineering Student  
Thapar Institute of Engineering & Technology

GitHub: https://github.com/harshitjain-2605

---

## ⭐ Skills Demonstrated

- Machine Learning
- Fraud Detection
- Data Analytics
- Feature Engineering
- Predictive Modeling
- SQL Analysis
- Risk Analytics
- Data Visualization
- Data Quality Management
- Model Evaluation
- Business Problem Solving
- End-to-End Data Science Workflow
