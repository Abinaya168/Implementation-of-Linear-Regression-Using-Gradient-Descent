# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Initialize slope mmm, intercept bbb, learning rate, and iterations. 2.Compute predicted values using y^=mx+b\hat{y} = mx + by^​=mx+b. 3.Calculate error between actual and predicted values. 4.Update mmm and bbb using gradient descent formulas. 5.Repeat until the error is minimized (convergence).

## Program:

/*
Program to implement the linear regression using gradient descent.
Developed by: P.Abinaya
RegisterNumber:25014594  
*/
```

import numpy as np
import matplotlib.pyplot as plt

# Sample dataset (X = input, y = output)
X = np.array([1, 2, 3, 4, 5], dtype=float)
y = np.array([2, 4, 5, 4, 5], dtype=float)

# Initialize parameters
m = 0  # slope
b = 0  # intercept

# Hyperparameters
learning_rate = 0.01
epochs = 1000
n = len(X)

# Gradient Descent
for i in range(epochs):
    y_pred = m * X + b
    
    # Compute gradients
    dm = (-2/n) * np.sum(X * (y - y_pred))
    db = (-2/n) * np.sum(y - y_pred)
    
    # Update parameters
    m = m - learning_rate * dm
    b = b - learning_rate * db

# Final parameters
print("Slope (m):", m)
print("Intercept (b):", b)

# Predictions
y_pred = m * X + b

# Plot
plt.scatter(X, y, color='blue', label='Actual Data')
plt.plot(X, y_pred, color='red', label='Regression Line')
plt.xlabel("X")
plt.ylabel("y")
plt.legend()
plt.show()
*/
```

## Output:
![linear regression using gradient descent](sam.png)
<img width="1108" height="819" alt="image" src="https://github.com/user-attachments/assets/8eaf2138-4be6-472a-b27b-9c1f856c4c34" />


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
