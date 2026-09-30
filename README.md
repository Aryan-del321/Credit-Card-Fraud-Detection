# Credit Card Fraud Detection

## Project Overview

This project uses machine learning to detect fraudulent credit card transactions. The dataset is highly imbalanced, with fraud transactions representing only a very small portion of all transactions.

The project focuses on building and evaluating a fraud detection model using appropriate evaluation metrics such as Precision, Recall, F1-Score, Confusion Matrix, and ROC-AUC.

## Dataset

* Total transactions: 284,807
* Normal transactions: 284,315
* Fraud transactions: 492
* Features: 30
* Target column: `Class`

  * `0` → Normal transaction
  * `1` → Fraudulent transaction

The dataset is highly imbalanced, so accuracy alone is not sufficient for evaluating the model.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook

## Project Workflow

1. Load and understand the dataset
2. Analyze class imbalance
3. Split data into training and testing sets
4. Preprocess the data
5. Train Logistic Regression
6. Train Random Forest
7. Generate predictions
8. Evaluate using Confusion Matrix
9. Analyze Precision, Recall and F1-Score
10. Calculate ROC-AUC
11. Plot ROC Curve
12. Analyze Random Forest feature importance

## Model Evaluation

The Random Forest model produced the following confusion matrix:

```text
[[56859     5]
 [   18    80]]
```

From the confusion matrix:

* True Negatives: 56,859
* False Positives: 5
* False Negatives: 18
* True Positives: 80

Fraud detection results derived from the confusion matrix:

* Precision: ~94.1%
* Recall: ~81.6%

### ROC-AUC

```text
ROC-AUC: 0.963
```

ROC-AUC was used because the dataset is highly imbalanced and accuracy alone can be misleading.

## Feature Importance

Random Forest feature importance was analyzed to understand which features were most useful for the model.

The most important features included:

* V17
* V14
* V12
* V10
* V16
* V11

The dataset contains anonymized features (`V1`–`V28`), so their real-world meanings are not interpreted in this project.

## Key Learning

This project helped me understand:

* Imbalanced classification
* Fraud detection
* Train/test splitting
* Classification models
* Confusion matrix
* Precision and Recall
* F1-Score
* ROC-AUC
* ROC Curve
* Feature importance
* Why accuracy alone is not enough for imbalanced datasets

## Project Structure

Credit-Card-Fraud-Detection/
│
├── Credit_Card_Fraud_Detection.ipynb
├── README.md



## Future Improvements

* Experiment with classification thresholds
* Handle class imbalance using techniques such as SMOTE
* Deploy the model using Streamlit
* Improve fraud detection while controlling false positives
