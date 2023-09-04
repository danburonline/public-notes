#core/machinelearning

Regression is a type of predictive modelling technique. It estimates the relationship between a dependent variable (outcome variable) and one or more independent variables (predictors).

## 1. K-Nearest Neighbours (KNN)

KNN is a non-parametric method used for classification and regression. In both cases, the input consists of the k closest training examples in the feature space.

Example:

```python
from sklearn.neighbors import KNeighborsRegressor

knn = KNeighborsRegressor(n_neighbors=3)
knn.fit(X_train, y_train)
predictions = knn.predict(X_test)
```

## 2. Linear Regression

Linear regression is used to predict an outcome variable that is continuous in nature. It assumes a linear relationship between the outcome variable and the predictors.

Example:

```python
from sklearn.linear_model import LinearRegression

lin_reg = LinearRegression()
lin_reg.fit(X_train, y_train)
predictions = lin_reg.predict(X_test)
```

Squared values (like R-squared) are often used to indicate the accuracy of a linear regression model.

## 3. Lasso Regression

Lasso (Least Absolute Shrinkage and Selection Operator) regression is a type of linear regression that uses shrinkage, where data values are shrunken towards a central point, like the mean.

Example:

```python
from sklearn.linear_model import Lasso

lasso_reg = Lasso(alpha=0.1)
lasso_reg.fit(X_train, y_train)
predictions = lasso_reg.predict(X_test)
```

## 4. Ridge Regression

Ridge Regression is a technique used when the data suffers from multicollinearity (independent variables are highly correlated). In multicollinearity, even though the least squares estimates (OLS) are unbiased, their variances are large, which deviates the observed value far from the true value.

Example:

```python
from sklearn.linear_model import Ridge

ridge_reg = Ridge(alpha=1.0)
ridge_reg.fit(X_train, y_train)
predictions = ridge_reg.predict(X_test)
```

## 5. Logistic Regression

Logistic Regression is a Machine Learning algorithm which is used for the classification problems, it is a predictive analysis algorithm and based on the concept of probability.

Example:

```python
from sklearn.linear_model import LogisticRegression

log_reg = LogisticRegression()
log_reg.fit(X_train, y_train)
predictions = log_reg.predict(X_test)
```

---

## Model Evaluation Metrics

- **Precision**: Precision is the ratio of correctly predicted positive observations to the total predicted positives.
- **Recall (Sensitivity)**: Recall is the ratio of correctly predicted positive observations to all observations in the actual class.
- **F1-Score**: The F1 Score is the weighted average of Precision and Recall. Therefore, this score takes both false positives and false negatives into account.
- **Support**: Support is the number of actual occurrences of the class in the specified dataset.

Example:

```python
from sklearn.metrics import classification_report

print(classification_report(y_test, predictions))
```

This will print out the precision, recall, f1-score and support for each class in your dataset.
