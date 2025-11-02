# 📘 ICS1502 - Introduction to Machine Learning  
### CAT Assignment 1  
**Sri Sivasubramaniya Nadar College of Engineering, Chennai**  
*(An Autonomous Institution affiliated to Anna University)*  
**Department of Computer Science and Engineering**  

---

### 🧾 Student Details
- **Name:** M K Kawvya  
- **Register No:** 3122237001022  
- **Batch:** 2023–2028  
- **Semester:** V  
- **Degree & Branch:** M.Tech (Integrated) Computer Science and Engineering  
- **Academic Year:** 2025–2026 (Odd Semester)

---

## 🎯 AIM
To implement and critically evaluate **Linear Regression** and **Linear Classification (Logistic Regression)** techniques using matrix-based and gradient-based approaches on real-world datasets — the *Mobile Phone Price Prediction* and *Bank Note Authentication* datasets.

---

## 🧩 OBJECTIVES
1. Construct data and label matrices suitable for regression and classification tasks.  
2. Apply both closed-form and gradient descent methods for Linear Regression.  
3. Implement Logistic Regression with and without L2 Regularization.  
4. Evaluate the effect of regularization and data standardization on model performance.  
5. Analyze model performance using prediction accuracy, Mean Squared Error (MSE), and R² metrics.  
6. Study the robustness of classifiers under the influence of outliers.  

---

## 🧰 LIBRARIES USED
```python
numpy
pandas
matplotlib
seaborn
sklearn (for preprocessing and evaluation metrics)


🧮 PART I — Linear Regression (Mobile Phone Price Prediction)
📊 Dataset Overview

The dataset includes several numerical features describing smartphone specifications and a target variable representing price range (0–3).
No missing values were found. Outliers were detected and treated using interquartile range filtering.

⚙️ Methods Implemented

Closed-form Solution:
Used matrix pseudo-inverse formula

w=(XTX)−1XTy

Gradient Descent Optimization:
Iteratively updated weights to minimize MSE.

Ridge Regression (L2 Regularization):
Added λI to reduce overfitting.

Standardization:
Compared performance with and without feature scaling.

📈 Performance Evaluation

| Model                                         | MSE    | R²     |
| --------------------------------------------- | ------ | ------ |
| Ridge Regression (λ=10, No Standardization)   | 0.1047 | 0.9215 |
| Ridge Regression (λ=10, With Standardization) | 0.1049 | 0.9214 |

Inference:
The model’s performance is nearly identical across both versions, suggesting that scaling had minimal influence. RAM and battery power were found to be the most influential predictors.

🧠 PART II — Linear Classification (Bank Note Authentication)
📊 Dataset Overview

The dataset contains 4 continuous statistical features extracted from banknote images and a binary class label (authentic or forged).
The data was normalized to improve training stability.

⚙️ Implementation Details

Implemented Logistic Regression from scratch using sigmoid activation.

Compared performance with and without L2 regularization.

Used gradient descent optimization for parameter learning.
Without L2: Test Accuracy = 0.9375
With L2=0.1: Test Accuracy = 0.9531

📉 Outlier Analysis

| Condition     | Test Accuracy |
| ------------- | ------------- |
| Original Data | 0.9375        |
| With Outliers | 0.8594        |

Conclusion:
Outliers caused a noticeable performance drop, indicating that Logistic Regression is sensitive to extreme values. Regularization and preprocessing are essential for robust performance.

📊 OUTPUTS SUMMARY

Regression:

MSE = 0.1047, R² = 0.9215

Ridge regularization improved stability and reduced overfitting.

Classification:

Accuracy improved from 93.75% → 95.31% with L2 regularization.

Outliers reduced accuracy by ~8%, showing model sensitivity.

Feature Importance:

RAM and battery power most strongly influenced mobile price.

🧠 LEARNING OUTCOMES

Understood mathematical derivations behind Linear and Logistic Regression.

Learned to implement models from scratch using NumPy and matrix operations.

Compared closed-form vs gradient-based optimization methods.

Observed how regularization (L2) improves model generalization.

Gained hands-on experience in data cleaning, standardization, and visualization.

Developed interpretation skills for feature importance and model evaluation.
