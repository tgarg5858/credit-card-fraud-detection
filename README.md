# 💳 Credit Card Fraud Detection

A machine learning project that detects **fraudulent credit card transactions** using **Logistic Regression**.
The system is deployed as an **interactive web app** with **Streamlit**, where users can input transaction details and get predictions in real time.

---

## 🚀 Features

* Preprocesses highly imbalanced fraud dataset (undersampling used).
* Trains a **Logistic Regression** model on balanced data.
* Evaluates model with **accuracy score** on training & testing sets.
* Streamlit-based web interface for **real-time predictions**.
* User can enter transaction features manually to classify as **Legitimate** or **Fraudulent**.

---

## 📂 Project Structure

```
credit-card-fraud-detection/
│── credit_fraud_app.py   # Main Streamlit app (your code)
│── creditcard.csv        # Dataset (Kaggle Credit Card Fraud Dataset)
│── README.md             # Documentation
```

---

## ⚙️ Requirements

Install the required dependencies:

```bash
pip install numpy pandas scikit-learn streamlit
```

---

## 🖥️ Usage

### 1️⃣ Run the App

```bash
streamlit run credit_fraud_app.py
```

### 2️⃣ Input Features

* Paste **comma-separated values** for all features (V1, V2, …, V28, Amount, etc.).
* Example input (must match dataset feature count):

  ```
  -1.3598071336738,-0.0727811733099,2.5363467379691,1.3781552242744,-0.338320769942,0.4623877777623,0.2395985540612,0.098697901261,0.3637869696112,0.0907941719785,-0.5515995332608,-0.6178008557623,-0.991389847235,1.9493588690805,-0.4146507811165,-0.5630283073351,-0.3104992261889,1.6693732754612,0.5172323708618,-0.165945923738,1.449043781147, -1.176338825359,0.913859823635, -1.37566665356, -0.638671952771,0.101288021253, -0.339846475529,0.167170404418,0.125894532368,149.62
  ```

### 3️⃣ Prediction Output

* **Legitimate transaction** ✅
* **Fraudulent transaction** ❌

---

## 📊 Model Details

* **Algorithm**: Logistic Regression
* **Training Data**: Undersampled balanced dataset (equal legit & fraud samples)
* **Accuracy**:

  * Training: \~`train_acc`
  * Testing: \~`test_acc`

---

## 🔒 Notes

* Dataset used: [Kaggle Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud)
* All **30 features** (V1–V28, Time, Amount) are required for prediction.
* The dataset is **heavily imbalanced** (majority legitimate → undersampling applied).

---

## 🛠️ Future Improvements

* Use **SMOTE** or advanced resampling instead of undersampling.
* Try **Random Forest, XGBoost, or Neural Networks** for better accuracy.
* Add **ROC curve, Precision, Recall, and F1-score** metrics to evaluation.
* Secure the app with user authentication.
* 
