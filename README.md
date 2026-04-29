# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1. **Import libraries and define dataset** (X = hours studied, Y = marks scored).
2. **Train Linear Regression model** using `model.fit(X, Y)`.
3. **Predict marks** for user-given hours using `model.predict()`.
4. **Plot graph** showing actual data points and the regression line.

 

## Program:
```

Program to implement the simple linear regression model for predicting the marks scored.
Developed by: NIVASH P
RegisterNumber:  212225230203
```
```
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([35, 50, 65, 70, 85])
model = LinearRegression()
model.fit(X, Y)
m = model.coef_[0]
b = model.intercept_
print("Slope (m):", m)
print("Intercept (b):", b)
x = float(input("Enter the number of hours studied: "))
marks = model.predict([[x]])
print("Predicted Marks for the Number of hours studied is:", marks[0])
Y_pred = model.predict(X)
plt.scatter(X, Y, label=" Actual Data points")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("No. of Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Implementation of Simple Linear Regression Model for Predicting the Marks Scored")
plt.legend()
plt.show()
```

## Output:
<img width="950" height="652" alt="image" src="https://github.com/user-attachments/assets/02da1347-0e2b-4cd9-acd6-173921e715ff" />



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
