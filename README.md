# Consumer-Churn-Prediction
Machine Learning Project

# Consumer_Classification

## 📌 Project Overview

**Consumer_Classification** is a machine learning project developed for **CSE422L: Artificial Intelligence Lab** (Section 12, Spring 2024). The objective of this project is to build predictive models that classify consumers based on their likelihood to churn (i.e., stop purchasing). This classification helps businesses implement data-driven marketing strategies and better understand consumer behavior.

---

## 👥 Group Information

| Name                    |
|-------------------------|
| Ummay Maimona Chaman    |
| Tahrim Showkat          |

---

## 🗂️ Table of Contents

- [Dataset](#Dataset)
- [EDA Summary](#eda-summary)
- [Preprocessing](#preprocessing)
- [Modeling](#modeling)
- [Results](#results)
- [Conclusion](#conclusion)
- [Future Work](#future-work)
- [How to Run](#how-to-run)
- [Project Links](#project-links)

---

## 📊 Dataset

- **Source**: [Google Drive](https://drive.google.com/file/d/1pg5z2_6OJsdd7VxGEfa8oXAihYq1KYtV/view)
- **Size**: 1500 records
- **Features**: 9 (both numerical and categorical)
- **Target**: Binary (`Churn` → 0: Not Churned, 1: Churned)
- **Balanced?**: Yes (Approx. 50/50 split)

### Key Features

- Demographic: `Age`, `Gender`, `Marital_Status`
- Behavioral: `Num_Purchase`, `Membership_Years`, `Device_Used`
- Financial: `Income`, `Credit_Score`

---

## 📈 EDA Summary

- Younger individuals and those with lower income/credit scores tend to churn more.
- Mobile device users show higher churn rates.
- Marital status plays a role: Single users churn more frequently.
- Most variables have weak correlation, indicating multifactorial influence on churn behavior.

---

## 🧹 Preprocessing

- **Missing Values**:
  - Imputed using `median` (numerical) and `mode` (categorical)
- **Encoding**:
  - Used `Label Encoding` for `Gender`, `Marital_Status`, `Device_Used`
- **Scaling**:
  - Applied `StandardScaler` to standardize numeric features
- **Splitting**:
  - Train/Test split (70/30) with **Stratified Sampling** to preserve class distribution

---

## 🤖 Modeling

Four classification models were trained and evaluated:

1. **K-Nearest Neighbors**
   - `k=5`, Euclidean distance
   - Accuracy: 49.33%

2. **Decision Tree**
   - Criterion: Gini
   - Accuracy: 50.00%

3. **Naive Bayes**
   - GaussianNB
   - Accuracy: 52.44%

4. **Neural Network**
   - Architecture: Input(14) → Hidden(32→16) → Output(1, Sigmoid)
   - Optimizer: Adam | Epochs: 50 | Batch Size: 32
   - Accuracy: 52.89%
   - AUC: 0.5259

---

## 📊 Results

| Model          | Accuracy | Precision | Recall | F1-Score |
|----------------|----------|-----------|--------|----------|
| KNN            | 49.33%   | 49%       | 49%    | 49%      |
| Decision Tree  | 50.00%   | 50%       | 50%    | 50%      |
| Naive Bayes    | 52.44%   | 52%       | 52%    | 52%      |
| Neural Network | **52.89%** | **52%**   | **53%**| **53%**  |

> 🔍 **Neural Network outperformed others**, but all models showed marginal improvements over random guessing.

---

## 🧾 Conclusion

- The best model (Neural Network) achieved only ~53% accuracy, suggesting **limited predictive power** from the existing features.
- Stronger predictive models likely require **richer consumer data** (e.g., browsing behavior, purchase history).

---

## 🚀 Future Work

- Use **Ensemble Models** (e.g., Gradient Boosting, Random Forest)
- Explore **Deeper Neural Networks**
- Add features like:
  - Social media engagement
  - Time of last purchase
  - Session duration or clickstream data

---

## 💻Friendly Information:

Feel free to use or adapt this system to suit your needs. If you make any modifications or use this project, we’d love to hear how you implemented it. We’re happy to assist further! :)

If you encounter any issues or have questions, don’t hesitate to reach out to us. :)

Best Regards,
Ummay Maimona Chaman
Tahrim Showkat    
