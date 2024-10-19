# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```

Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Kalaiselvan J
RegisterNumber:  212223080022

```

```
import numpy as np
import matplotlib.pyplot as plt

# Input data
X = np.array(eval(input("Enter the X values as a list : ")))
Y = np.array(eval(input("Enter the Y values as a list : ")))

# Calculate the means
X_mean = np.mean(X)
print(f"Mean of X values: {X_mean}")

Y_mean = np.mean(Y)
print(f"Mean of Y values: {Y_mean}")

# Initialize numerator and denominator for the slope calculation
num = 0
denum = 0

# Loop through to calculate numerator and denominator
for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i] - Y_mean)
    denum += (X[i] - X_mean) ** 2

# Calculate slope (m)
m = num / denum
print(f"Slope (m) of the regression line: {m}")

# Calculate intercept (b)
b = Y_mean - m * X_mean
print(f"Intercept (b) of the regression line: {b}")

# Calculate predicted Y values
Y_pred = m * X + b
print(f"Predicted Y values: {Y_pred}")

# Plot the data points and the regression line
plt.scatter(X, Y, color='blue', label='Original data')
plt.plot(X, Y_pred, color='yellow', label='Regression line')
plt.xlabel('X values')
plt.ylabel('Y values')
plt.title('Linear Regression')
plt.legend()
plt.show()

```














## Output:

![image](https://github.com/user-attachments/assets/861986b8-db78-4da9-8efe-f5bd8c1cc14a)

![image](https://github.com/user-attachments/assets/0c462dbd-bede-4868-8d8d-0648e4b23698)





## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
