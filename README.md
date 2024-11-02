# Credit Card Fraud Detection Using Logistic Regression and SVM

This project aims to detect credit card fraud by building and comparing two machine learning models: **Logistic Regression** and **Support Vector Machine (SVM)**. In fraud detection, it’s essential to catch fraudulent transactions effectively, so our focus is on **maximizing recall** — the model’s ability to identify fraud without missing cases.

## 📊 Dataset

We’re working with the **Credit Card Fraud Detection** dataset (`creditcardfraud.csv`), which includes anonymized features of transactions and labels indicating whether each transaction is fraudulent or legitimate.

## 🚀 Project Workflow

### 1. Data Preprocessing
   - **Drop the 'Time' column**: The time of the transaction doesn’t contribute to fraud detection, so it’s excluded.
   - **Scale the 'Amount' column**: The 'Amount' column is standardized to align with other features for model training.

### 2. Train-Test Split
   - The dataset is divided into **80% training** and **20% testing** data, using `random_state=42` for reproducibility.

### 3. Model Training
   - **Logistic Regression**: Trained with default parameters on the training data.
   - **SVM**: Trained with default parameters on the training data.

### 4. Model Evaluation
   - **Confusion Matrix**: Shows counts of correct and incorrect predictions, helping us understand true and false positives/negatives.
   - **Classification Report**: Provides **precision, recall, and F1-score** for each model, critical for understanding model performance on fraud detection.

### 5. Hyperparameter Tuning
   - **Grid Search Cross-Validation**: Conducted to optimize each model’s hyperparameters, targeting higher accuracy.
   - **Retraining with Optimal Hyperparameters**: Both models are retrained with the best parameters and evaluated on the test data.

### 6. Results & Comparison
   - **Key Metric — Recall**: Both models performed similarly in terms of accuracy, but **recall** revealed a significant difference. The Logistic Regression model achieved **higher recall**, identifying more fraudulent cases than the SVM.

## 📝 Findings and Conclusions

Both models showed comparable accuracy, but **Logistic Regression** demonstrated a clear advantage in recall:
   - **Logistic Regression Recall**: 0.9310
   - **SVM Recall**: 0.9138

Since **recall** is crucial in fraud detection (as missing fraud cases can have serious consequences), **Logistic Regression** is the preferred model. The higher recall means it’s better at identifying fraudulent transactions and reducing undetected cases.

---

### Summary

This project demonstrated how **Logistic Regression** and **SVM** can be applied to credit card fraud detection, with **recall** emphasized as the key metric for reducing undetected fraud cases. While both models had similar accuracy, **Logistic Regression's higher recall makes it the more effective choice**, highlighting the importance of selecting evaluation metrics that align with the task's goals.
