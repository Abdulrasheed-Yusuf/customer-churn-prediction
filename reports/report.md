# Customer Churn Prediction Report

## 1. Introduction
Customer churn prediction is a crucial task for businesses to retain customers by identifying those likely to leave. This project explores two models—Logistic Regression and a Neural Network—to predict customer churn using a structured dataset.

## 2. Data Preprocessing
The dataset underwent preprocessing, including:
- Handling missing values
- Encoding categorical variables
- Normalizing numerical features
- Splitting into training and test sets

## 3. Model Training and Evaluation

### 3.1 Logistic Regression Model
A Logistic Regression model was trained to serve as a baseline.

#### Training Set Performance:
- **Accuracy:** 0.748
- **Precision:** 0.516
- **Recall:** 0.802
- **F1-score:** 0.628

#### Test Set Performance:
- **Accuracy:** 0.757
- **Precision:** 0.526
- **Recall:** 0.828
- **F1-score:** 0.644

### 3.2 Neural Network Model
A Neural Network was implemented using TensorFlow and trained with multiple epochs for improved performance.

#### Training Set Performance:
- **Accuracy:** 0.819
- **Precision:** 0.668
- **Recall:** 0.636
- **F1-score:** 0.652

#### Test Set Performance:
- **Accuracy:** 0.806
- **Precision:** 0.637
- **Recall:** 0.617
- **F1-score:** 0.627

## 4. Model Comparison
- The **Logistic Regression** model performed well with an accuracy of 75.7% on the test set. However, its recall was higher than precision, indicating a higher false positive rate.
- The **Neural Network** outperformed the logistic model in accuracy and precision but had slightly lower recall.
- The Neural Network achieved better F1-scores, demonstrating a more balanced performance.

## 5. Model Saving and Visualization
To ensure reproducibility and future analysis:
- Both models were saved.
- Model weights and biases were stored.
- Classification reports were generated.
- Confusion matrices and ROC curves were plotted for evaluation.

## 6. Conclusion
The Neural Network model provided a slight improvement over Logistic Regression in terms of accuracy and precision. However, additional tuning, such as hyperparameter optimization and feature engineering, could further enhance model performance.

Future work includes:
- Fine-tuning hyperparameters using Grid Search or Bayesian Optimization.
- Exploring different architectures for the Neural Network.
- Deploying the best-performing model for real-world usage.

