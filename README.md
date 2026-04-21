# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard Libraries
2. Set variables for assigning dataset values.
3. Import linear regression from sklearn
4. Assign the points for representing in the graph
5. Predict the regression for marks by using the representation of the graph
6. Compare the graphs and hence we obtained the linear regression for the given datas.


## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Kamali V
RegisterNumber:  212225240066
*/
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
x_input = float(input("Enter hours studied: "))
predicted_marks = model.predict([[x_input]])
print("Predicted Marks:", predicted_marks[0])
Y_pred = model.predict(X)
plt.scatter(X, Y, label="Actual Data")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression (Using sklearn)")
plt.legend()
plt.show()
```

## Output:


<img width="746" height="681" alt="image" src="https://github.com/user-attachments/assets/dd020399-6cae-4bf0-a0a2-38e1170aa4db" />

## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
