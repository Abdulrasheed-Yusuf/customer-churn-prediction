# Customer Churn Prediction

## Project Overview

This project focuses on predicting customer churn using machine learning models. Two models—Logistic Regression and a Neural Network—were trained and evaluated to determine the best-performing model.

## Dataset

The dataset contains customer information and service details, with the target variable being **Churn** (Yes/No). Key features include:

- Demographic information (Gender, SeniorCitizen, etc.)
- Service subscription details (InternetService, Contract, PaymentMethod, etc.)
- Usage statistics (tenure, MonthlyCharges, TotalCharges)

## Data Preprocessing

- Missing values handled
- Categorical features encoded
- Numerical features normalized
- Dataset split into training and test sets

## Models Trained

### 1. Logistic Regression

- Used as a baseline model
- Performance:
  - **Accuracy:** 75.7% (Test set)
  - **Precision:** 52.6%
  - **Recall:** 82.8%
  - **F1-score:** 64.4%

### 2. Neural Network (TensorFlow)

- Achieved improved performance over Logistic Regression
- Performance:
  - **Accuracy:** 80.6% (Test set)
  - **Precision:** 63.7%
  - **Recall:** 61.7%
  - **F1-score:** 62.7%

## Model Comparison

| Metric    | Logistic Regression | Neural Network |
| --------- | ------------------- | -------------- |
| Accuracy  | 75.7%               | 80.6%          |
| Precision | 52.6%               | 63.7%          |
| Recall    | 82.8%               | 61.7%          |
| F1-score  | 64.4%               | 62.7%          |

- The **Neural Network** achieved **higher accuracy and precision**, indicating it better distinguishes between churn and non-churn customers.
- The **Logistic Regression model** had a **higher recall**, meaning it identified more actual churn cases, but at the cost of lower precision.
- The **Neural Network** provides a more balanced trade-off between precision and recall, making it more suitable for deployment.

## Model Saving

Both models were saved for future use:

- Logistic Regression model (`log_model.pkl`)
- Neural Network model (`model.h5`)
- Reports, weights, and biases saved separately

## How to Use

1. Clone the repository:
   ```sh
   git clone <repo-link>
   cd customer-churn-prediction
   ```
2. Run preprocessing and training:
   ```sh
   jupyter notebook
   ```
   Open and execute `churn_prediction.ipynb`
3. Load saved models for inference:

   ```python
   import pickle
   from tensorflow.keras.models import load_model

   # Load Logistic Regression model
   with open('log_model.pkl', 'rb') as f:
       log_model = pickle.load(f)

   # Load Neural Network model
   model = load_model('model.h5')
   ```
