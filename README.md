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
```
```
x=np.array(eval(input()))
```

![image](https://github.com/user-attachments/assets/a3239f5c-f5ac-41f3-8687-ac0594f7989f)
```
y=y=np.array(eval(input()))
```

![image](https://github.com/user-attachments/assets/d4201cc9-2d94-4714-b3c4-50cf36514457)
```
xmean=np.mean(x)
xmean
```

![image](https://github.com/user-attachments/assets/d7e46bb5-50ad-457e-b7e9-54ae0367542d)
```
ymean=np.mean(y)
ymean
```

![image](https://github.com/user-attachments/assets/12b6cb5e-af87-4096-9544-3a2545fc9ec0)
```
num=0
denom=0
```
```
for i in range(len(x)):
  num+=(x[i]-xmean)*(y[i]-ymean)
  denom+=(x[i]-xmean)**2
```
```
num
```

![image](https://github.com/user-attachments/assets/7dfbe70a-8187-4946-abd5-683784c70461)
```
denom
```

![image](https://github.com/user-attachments/assets/39dd9474-0063-4c0e-903a-428a2ea38880)
```
m=num/denom
m
```

![image](https://github.com/user-attachments/assets/a201d40f-a3cb-464b-a892-72e75b2679ce)
```
b=ymean-m*xmean
b
```

![image](https://github.com/user-attachments/assets/b353270f-601f-47b3-a77a-6cdde19f3008)
```
ypred=m*x+b
ypred
```

![image](https://github.com/user-attachments/assets/c47cefbb-5b1c-4e1a-a1d5-01afbc4eb7b4)
```
import matplotlib.pyplot as plt
```
```
plt.scatter(x,y)
plt.plot(x,ypred,color='green')
plt.show()
```














## Output:

![image](https://github.com/user-attachments/assets/3497e2a7-889a-4c96-a7b4-de00fd09cb15)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
