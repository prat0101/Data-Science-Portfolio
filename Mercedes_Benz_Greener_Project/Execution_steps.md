
# Execution Steps during Mercedes Benz Greener Project.


Execution steps:
1)	Import data
2)	Check Outliers for the predicted variable.
3)	Check the types of data structure
4)	Check for null values.
5)	Check the columns with minimum variance, remove them (Only for Binary columns)
a.	Variance thresholding

6)	Check multicollinearity (VIF) or correlation method. Check if to remove multicollinear columns. Use the Correlation method (Kendall) to remove multicollinearity for Categorical variables. We cannot use VIF for categorical variables.
7)	PCA should be used with correlated columns only. as we removed correlated columns, we should not use PCA on the variables. Also, PCA is not recommended to be used for categorical variables as it is based on the variability of the values in the column.
8)	Use the ‘get dummies‘ method to convert categorical variables to numeric ones. Limit it to maximum occurring categories. (Only for columns with ‘char’ data type)
9)	Split the data: train_test_Split.
### 10.	Using Linear Regression:
a.	Used Linear Regression first, then used Regularization to improve r2 value (Noticed significant change). Used Grid search CV to find the best value of alpha. Also used the Validation curve method.

### 11)	Using Gradient Boosting Algo:
a.	Hyperparameter tuning by using grid search CV, verifying the scores, and checking the overfitting by cross-validation.

b.	Using the Validation curve to check overfitting and parameter tuning.

c.	Fit the model with trained parameters on X_train and Y_train, Predict the values for X_test and check the metrics.

### 12)	Using XGboost:
a.	Using the same procedure for hyperparameter tuning as that used for Gradient boosting. Check the metrics and overfitting.

b.	After using XGboost, see the feature importance. If you don’t get the expected metrics, then use only the important features to improve the results.

c.	Fit the model with trained parameters on X_train and Y_train, Predict the values for X_test and check the metrics.

13)	Check the metrics after selecting important features from feature importance.
14)	Feature importance. (To decide important variables that affect the testing time). 

## Important References:
1. Checking the variance of column and remove the columns with zero variance.
(https://towardsdatascience.com/how-to-use-variance-thresholding-for-robust-feature-selection-a4503f2b5c3f)

2. Identify and remove multicollinear columns. https://www.analyticsvidhya.com/blog/2020/03/what-is-multicollinearity/ (VIF for numneric columns)

3. How to handle columns with large number of categories (https://www.youtube.com/watch?v=6WDFfaYtN6s&list=PLZoTAELRMXVPwYGE2PXD3x0bfKnR0cJjN)
