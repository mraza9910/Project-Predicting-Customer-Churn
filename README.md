# 📉 Customer Churn Prediction
This project focuses on identifying drivers of customer churn and building predictive models to help a business proactively retain at-risk customers.

# 📁 Dataset Overview
The dataset contains customer information including:
* Credit Score, Age, Tenure, Balance
* Product Ownership, Credit Card Status
* Activity Level, Estimated Salary
* Geography and Gender
* Churn Status 

# 🎯 Objectives
* Understand key factors contributing to customer churn
* Build and evaluate classification models to predict churn
* Use cross-validation and ROC-AUC metrics for model selection
* Provide actionable business insights based on model results

# 🧪 Methods & Tools
## 🔧 Preprocessing & EDA
* Data cleaned using pandas and visualized with seaborn/matplotlib
* Feature engineering included:
  * BalanceSalaryRatio = Balance / Salary
  * TenureByAge = Tenure / Age
  * One-hot encoding for categorical features (e.g., geography, gender)

# 🤖 Modeling
* Models used:
  * Logistic Regression (L2 Regularized)
  * Random Forest Classifier

## Tuning done via GridSearchCV:
* 5-fold cross-validation
* Best hyperparameters selected using AUC score

# 📊 Evaluation
* Used ROC-AUC to evaluate probability-based predictions
* Generated ROC curves for visual performance comparison
* Calculated Confusion Matrix, Precision, Recall, and F1

✅ Results Summary
* Random Forest slightly outperformed logistic regression on AUC
* Logistic Regression had a higher recall rate - best model
* Key churn predictors: Credit Score, Age, Balance, Geography
