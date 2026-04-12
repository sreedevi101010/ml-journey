# 📩 SMS Spam Classifier (NLP Project)

## 🚀 Overview

This project builds a machine learning model to classify SMS messages as **Spam** or **Not Spam (Ham)** using Natural Language Processing techniques.

It demonstrates how raw text data can be transformed into numerical features and used for classification.

---

## 🎯 Problem Statement

Can we automatically detect whether a message is spam or not based on its content?

This is a **binary classification problem**:

* `0 → Not Spam (Ham)`
* `1 → Spam`

---

## 📂 Dataset

* SMS Spam Collection Dataset
* Contains labeled SMS messages:

  * `ham` → normal messages
  * `spam` → promotional or fraudulent messages

---

## ⚙️ Approach

### 1. Data Preprocessing

* Selected relevant columns
* Renamed columns to `label` and `message`
* Converted labels:

  * `ham → 0`
  * `spam → 1`

---

### 2. Text Vectorization

Used **TF-IDF (Term Frequency–Inverse Document Frequency)** to convert text into numerical features.

---

### 3. Model Training

Used **Multinomial Naive Bayes**, which is highly effective for text classification tasks.

---

## 📊 Results

### ✅ Accuracy

```
96.14%
```

---

### 📈 Classification Report

| Class    | Precision | Recall | F1-score |
| -------- | --------- | ------ | -------- |
| Ham (0)  | 1.00      | 0.71   | 0.83     |
| Spam (1) | 0.96      | 1.00   | 0.98     |

---

## 🔍 Key Insights

* The model achieves **perfect recall (1.00)** for spam detection, meaning no spam messages are missed.
* Some normal messages are incorrectly classified as spam (lower recall for ham).
* This trade-off is acceptable because:

  * Missing spam is more harmful than misclassifying normal messages.
* The dataset is imbalanced, with more spam samples than ham.

---

## 🧠 Concepts Used

* Natural Language Processing (NLP)
* TF-IDF Vectorization
* Naive Bayes Classification
* Precision, Recall, F1-score
* Confusion Matrix

---

## 🔮 Sample Predictions

```python
predict_message("Congratulations! You won a free iPhone")
# Output: Spam

predict_message("Hey, are we meeting today?")
# Output: Not Spam
```

---

## 💾 Model Saving

Both model and vectorizer were saved using `pickle`:

* `spam_model.pkl`
* `vectorizer.pkl`

---

## 🧪 How to Run

```bash
pip install pandas numpy scikit-learn
```

```python
python notebook.ipynb
```

---

## 🔮 Future Improvements

* Use advanced models (Logistic Regression, SVM)
* Try deep learning (LSTM, Transformers)
* Deploy as a web application
* Add real-time prediction interface

---

## 🙌 Learnings

* How to process and vectorize text data
* Importance of evaluation metrics beyond accuracy
* Trade-offs between precision and recall
* Building end-to-end NLP pipelines

---

## 👩‍💻 Author

Vava
Computer Science Engineering Student
NIT Calicut

---

⭐ If you found this useful, feel free to star the repo!

