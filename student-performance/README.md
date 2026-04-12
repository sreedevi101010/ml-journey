# 🎓 Student Performance Predictor

## 🚀 Overview

This project predicts a student’s final grade (**G3**) based on behavioral and background factors such as study time, past failures, absences, and parental education.

The goal is to understand how different machine learning models perform on real-world educational data.

---

## 🎯 Problem Statement

Can we predict student performance using lifestyle and academic features?

This is a **regression problem**, where the output is a continuous value (final grade).

---

## 📂 Dataset

* Student Performance Dataset
* Contains student information like:

  * Study time
  * Number of past failures
  * Absences
  * Parental education
  * Social and health factors

---

## ⚙️ Features Used

To avoid **data leakage**, only pre-performance features were used:

* `studytime`
* `failures`
* `absences`
* `Medu` (mother’s education)
* `Fedu` (father’s education)

> ❗ Features like `G1` and `G2` were intentionally excluded since they directly influence the final grade.

---

## 🤖 Models Implemented

### 1. Linear Regression

* Baseline model
* Simple and interpretable

### 2. Decision Tree Regressor

* Captures non-linear relationships
* Prone to overfitting on small datasets

### 3. Ridge Regression

* Linear model with regularization
* Helps reduce overfitting

---

## 📊 Results

| Model             | R² Score | MSE    |
| ----------------- | -------- | ------ |
| Linear Regression | 0.17     | ~10.28 |
| Decision Tree     | -0.27    | ~11.98 |
| Ridge Regression  | 0.11     | ~8.35  |

---

## 🔍 Key Insights

* Linear Regression performed best in explaining variance.
* Ridge Regression achieved lower error (better prediction stability).
* Decision Trees performed poorly due to weak feature relationships and dataset noise.
* Simpler models can outperform complex ones when features are limited.

---

## 📈 Visualization

Scatter plot of Actual vs Predicted values was used to evaluate model performance.

---

## 💾 Model Saving

All models were saved using `pickle` for reuse:

* `linear_model.pkl`
* `decision_tree_model.pkl`
* `ridge_model.pkl`

---

## 🧪 How to Run

```bash
pip install pandas numpy scikit-learn matplotlib
```

```python
python notebook.ipynb
```

---

## 🔮 Future Improvements

* Add more relevant features
* Perform feature engineering
* Use ensemble models (Random Forest, XGBoost)
* Deploy as a web app

---

## 🙌 Learnings

* Importance of feature selection
* Trade-off between bias and variance
* Model comparison and evaluation
* Real-world ML workflow

---

## 👩‍💻 Author

Vava
Computer Science Engineering Student
NIT Calicut

---

⭐ If you found this useful, feel free to star the repo!

