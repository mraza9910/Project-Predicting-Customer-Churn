# 📉 Customer Churn Prediction
This project focuses on identifying drivers of customer churn and building predictive models to help a business proactively retain at-risk customers.

# 🧰 Tools & Technologies
* Python, Pandas, NumPy
* Scikit-learn for ML modeling
* Matplotlib, Seaborn for visualizations
* Jupyter Notebook for experimentation and analysis

# 📁 Dataset Overview
The dataset contains customer information including:
* Credit Score, Age, Tenure, Balance
* Product Ownership, Credit Card Status
* Activity Level, Estimated Salary
* Geography and Gender
* Churn Status 

# 🎯 Objectives
* Understand key factors contributing to customer churn
* Build and evaluate classification models to predict likelihood of a customer churning
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
* Used both ROC-AUC and confusion matrix-based metrics to evaluate model performance on the test set.

# Business Insights and Proposed Solutions/Impact:
* Countries with lower number of customers, such as Germany, have a high churn rate. **Solution**: Perhaps the bank is not allocating required resources to the territories with the least number of customers?
* Females churn more often than the males. **Solution**: Implement programs targeting female customer retention. For example, assign bonuses when a female opens an account.
* Older customers churn more often than the younger customers. **Solution**: Revise target market, or design strategies for older customer retention.
* Customers with a higher account balance churn more. **Impact**: Negatively impacts the capital available for lending.
* Customers with the shortest and longest tensure with the bank churn the most.
* Customers with a credit card churn the most.

# 🏆 Best Model: Logistic Regression
Although the Random Forest achieved a slightly higher AUC, the Logistic Regression model was selected as the final model due to:

* Better precision–recall balance
* Simplicity and interpretability, which are key for explaining churn behavior to stakeholders

# 📌 Next Steps
* To further boost predictive performance, build XGBoost, SMOTE models as they tend to handle class imbalance effectively
* Test with newer data to ensure generalization
