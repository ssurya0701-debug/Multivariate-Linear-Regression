# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
import pandas as pd.

### Step2
Read the csv file.

### Step3
Get the value of X and y variables

### Step4
Create the linear regression model and fit

### Step5
Predict the CO2 emission of a car where the weight is 2300kg, and the volume is 1300cm cube

## Program:
```
import numpy as np
import matplotlib.pyplot as plt

# Preprocessing input data
X = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
Y = np.array([1, 3, 2, 5, 7, 8, 8, 9, 10, 12])

plt.scatter(X, Y)
plt.show()

# Building the model
X_mean = np.mean(X)
Y_mean = np.mean(Y)

num = 0
den = 0

for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i] - Y_mean)
    den += (X[i] - X_mean) ** 2

m = num / den
c = Y_mean - m * X_mean

print(m, c)

# Making predictions
Y_pred = m * X + c
print(Y_pred)

plt.scatter(X, Y)  # Actual
plt.scatter(X, Y_pred, color="red")
plt.plot([min(X), max(X)], [min(Y_pred), max(Y_pred)], color="red")  # Predicted
plt.show()





```
## Output:
<img width="752" height="600" alt="image" src="https://github.com/user-attachments/assets/1f249ec4-3b79-4575-9486-4a12afe9ee20" />

<img width="750" height="537" alt="image" src="https://github.com/user-attachments/assets/ddda7ce6-8538-4871-9e4d-848fbe98cbcd" />



## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
