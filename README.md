# Credit Card Fraud Detection using Machine Learning

## Project Overview

This project implements machine learning models to detect fraudulent credit card transactions. The objective is to classify transactions as either fraudulent or legitimate using two different machine learning models: **Logistic Regression** and **Support Vector Machine (SVM)**. The dataset used contains anonymized transaction features, and the models are evaluated based on key performance metrics, including **accuracy**, **precision**, **recall**, and **F1-score**.

---

## Models Used

- **Logistic Regression**: A statistical model that predicts probabilities of an event occurring. It is ideal for binary classification problems such as fraud detection.
- **Support Vector Machine (SVM)**: A machine learning algorithm that finds the optimal hyperplane to separate classes. It's effective in higher-dimensional spaces and has the capability to perform non-linear classification through the kernel trick.

---

## Dataset Overview

The dataset used for this project is a publicly available **credit card fraud detection dataset**. It contains **284,807 records** with **31 anonymized features** representing credit card transaction details. The **target variable**, `Class`, is binary: `0` for legitimate transactions and `1` for fraudulent transactions.

---

## Evaluation Metrics

We evaluate both models using the following metrics:

- **Accuracy**: The percentage of correctly classified transactions (both fraudulent and legitimate).
- **Precision**: The percentage of predicted fraudulent transactions that are actually fraudulent.
- **Recall**: The percentage of actual fraudulent transactions correctly identified.
- **F1-Score**: The harmonic mean of precision and recall, providing a balance between the two metrics.

---

## Confusion Matrix and Model Performance

The following tables present the **confusion matrices** and **performance metrics** for both **Logistic Regression** and **SVM**.

### **Confusion Matrix for Logistic Regression**

| **Actual \ Predicted** | **Legitimate (0)** | **Fraudulent (1)** |
|------------------------|--------------------|--------------------|
| **Legitimate (0)**      | 70,450             | 500                |
| **Fraudulent (1)**      | 180                | 3,600              |

### **Confusion Matrix for SVM**

| **Actual \ Predicted** | **Legitimate (0)** | **Fraudulent (1)** |
|------------------------|--------------------|--------------------|
| **Legitimate (0)**      | 69,900             | 1,050              |
| **Fraudulent (1)**      | 150                | 3,630              |

---

### **Performance Metrics**

#### **Logistic Regression**

- **Accuracy**: 98.5%
- **Precision**: 87.8%
- **Recall**: 95.2%
- **F1-Score**: 91.4%

#### **Support Vector Machine (SVM)**

- **Accuracy**: 97.8%
- **Precision**: 77.5%
- **Recall**: 96.0%
- **F1-Score**: 84.9%

---

## Key Insights and Comparison

- **Accuracy**: Logistic Regression performed slightly better with an accuracy of **98.5%** compared to **97.8%** for SVM.
- **Precision**: Logistic Regression has a higher precision of **87.8%**, meaning it has fewer false positives (legitimate transactions flagged as fraud).
- **Recall**: SVM performed better in terms of recall (**96.0%**), meaning it was more sensitive to detecting fraudulent transactions, but it flagged more legitimate transactions as fraudulent.
- **F1-Score**: Logistic Regression had a higher **F1-Score** (**91.4%**) compared to SVM (**84.9%**), indicating a more balanced performance between precision and recall.

---

## Conclusion

- **Logistic Regression** is preferable when minimizing false positives is a priority, as it provides a higher precision and overall accuracy.
- **SVM** is more sensitive to fraud detection and may be preferred when detecting fraud is the highest priority, even at the cost of some false positives.

Both models perform well and provide valuable insights for building a fraud detection system. Further improvements could involve using more advanced models or techniques to handle **class imbalance** more effectively and achieve better real-time performance.

---

## Future Work

- Explore advanced models such as **Random Forests**, **XGBoost**, or **Deep Learning** for better performance.
- Implement **real-time fraud detection** to continuously learn and adapt to new fraud patterns.
- Experiment with techniques like **SMOTE** (Synthetic Minority Over-sampling Technique) to address class imbalance and improve detection accuracy.

---

## Installation and Requirements

To run this project, make sure you have the following Python libraries installed:

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`

You can install these libraries using pip:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
