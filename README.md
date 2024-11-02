# Credit Card Fraud Detection using Logistic Regression and SVM

This project involves building and evaluating two machine learning models — Logistic Regression and Support Vector Machine (SVM) — to predict whether a credit card transaction is fraudulent. The objective is to identify a model that provides high accuracy while ensuring reliable identification of fraudulent transactions, with an emphasis on maximizing recall to minimize false negatives.

## Dataset

We use the **Credit Card Fraud Detection dataset** (`creditcardfraud.csv`), which contains anonymized transaction data with labels indicating fraudulent or legitimate transactions.

## Project Steps

### 1. Data Preprocessing
- **Dropping the 'Time' column**: Since the time of the transaction is not relevant to classification, it is removed from the dataset.
- **Scaling the 'Amount' column**: The 'Amount' column is scaled using a standard scaler to ensure that feature scaling does not negatively affect model performance.

### 2. Data Splitting
- **Train-Test Split**: The dataset is split into training and test sets using an 80:20 ratio with `random_state=42` for reproducibility.

### 3. Model Training
- **Logistic Regression Model**: A Logistic Regression model is trained on the training set with default hyperparameters.
- **SVM Model**: An SVM model is trained on the training set with default hyperparameters.

### 4. Model Evaluation
- **Evaluation Metrics**: Both models are evaluated on the test set using:
  - **Confusion Matrix**
  - **Classification Report**: Includes metrics like precision, recall, and F1-score.

### 5. Hyperparameter Tuning
- **Grid Search Cross-Validation**: To enhance model performance, hyperparameters for both models are tuned using grid search cross-validation. The accuracy score is chosen as the evaluation metric during optimization.
- **Optimal Model Training**: Both Logistic Regression and SVM models are retrained with optimal hyperparameters, followed by evaluation on the test set.

### 6. Model Comparison and Insights
- Both models achieved similar accuracy; however, recall—a critical metric for fraud detection—revealed the Logistic Regression model’s superior performance. The Logistic Regression model achieved a recall of **0.9310**, while the SVM model reached **0.9138**. This indicates that Logistic Regression is better at identifying fraudulent transactions, making it a more reliable model for minimizing undetected fraud cases.

## Findings and Conclusions

In this analysis, **Logistic Regression outperformed SVM in recall** despite achieving similar overall accuracy. Since recall is a crucial metric in fraud detection, where minimizing false negatives is essential, Logistic Regression is preferred. Its ability to better detect fraudulent transactions with higher recall (0.9310 vs. 0.9138) makes it a suitable model for this task.

---

### Summary

This project illustrates the application of Logistic Regression and SVM for credit card fraud detection, emphasizing the importance of recall in fraud detection tasks. Logistic Regression demonstrated better performance by effectively identifying fraudulent cases, proving to be more suitable for this use case.
