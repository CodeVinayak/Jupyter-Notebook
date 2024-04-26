# Credit Risk Analysis Project

## Introduction
This project aims to build and evaluate a credit risk classification model using a dataset of historical lending activity from a peer-to-peer lending services company. The goal is to identify the creditworthiness of borrowers and predict the risk of loan default.

## Dataset
The dataset consists of the following features:

- `loan_size`: The size of the loan
- `interest_rate`: The interest rate of the loan
- `borrower_income`: The income of the borrower
- `debt_to_income`: The ratio of the borrower's debt to their income
- `num_of_accounts`: The number of accounts the borrower has
- `derogatory_marks`: The number of derogatory marks on the borrower's credit history
- `total_debt`: The total debt of the borrower
- `loan_status`: The target variable, indicating whether the loan is healthy (0) or high-risk (1)

## Steps

### 1. Data Exploration and Preprocessing
- Load the dataset
- Explore the dataset structure and statistics
- Split the data into features (X) and target (y)

### 2. Feature Engineering
- Scale the numerical features using StandardScaler

### 3. Handling Imbalanced Data
- Oversample the minority class (high-risk loans) using SMOTE

### 4. Model Training and Evaluation
- Split the resampled data into train and test sets
- Train a logistic regression model on the training data
- Evaluate the model's performance on the test data using classification report and confusion matrix

### 5. Hyperparameter Tuning
- Perform grid search cross-validation to tune the hyperparameters of the logistic regression model

### 6. Model Comparison
- Train a random forest classifier
- Calculate and compare the ROC AUC scores of logistic regression and random forest

### 7. Model Interpretability
- Calculate and print the feature importances using permutation importance

### 8. Exploratory Data Analysis (EDA)
- Generate a correlation matrix to visualize feature relationships
- Create a box plot for outlier detection

### 9. Feature Selection
- Compute mutual information between features and the target variable
- Select the top k features based on mutual information scores

### 10. Ensemble Methods (XGBoost)
- Train an XGBoost classifier
- Evaluate the XGBoost model's performance using the classification report

### 11. Hyperparameter Tuning (XGBoost)
- Perform randomized search cross-validation to tune the hyperparameters of the XGBoost model

### 12. Cross-Validation
- Perform 5-fold cross-validation for the logistic regression model
- Print the cross-validation scores and the mean score

### 13. Final Outcome
- Select the best-performing model (tuned XGBoost)
- Make predictions on the test data
- Print the final classification report

## Results
The final classification report shows that the tuned XGBoost model achieves an accuracy of 1.00 and perfect precision, recall, and F1-scores for both the healthy loan and high-risk loan classes. This indicates that the model is highly effective in predicting credit risk and identifying potential loan defaults.

## Conclusion
This project demonstrates a comprehensive approach to building and evaluating a credit risk classification model. It covers various techniques, including data preprocessing, feature engineering, handling imbalanced data, model training and evaluation, hyperparameter tuning, ensemble methods, and model interpretation. The use of advanced algorithms like XGBoost and thorough evaluation metrics showcase the ability to tackle complex problems and find the best-performing model for the given task.