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
Developed by: Jaden Samuel Abraham
Register Number: 212225040138

import numpy as np
import matplotlib.pyplot as plt
X=np.array([1,2,3,4,5])
Y=np.array([2,4,5,4,5])
mean_X=np.mean(X)
mean_Y=np.mean(Y)
m=np.sum((X-mean_X)*(Y-mean_Y))/np.sum((X-mean_X)**2)
b=mean_Y-(m*mean_X)
Y_pred=m*X+b
print("Slope:",m)
print("Intercept:",b)
print("Linear Regression Equation: Y =",m,"X +",b)
plt.scatter(X,Y,color='blue',label='Actual Data')
plt.plot(X,Y_pred,color='red',label='Best Fit Line')
plt.xlabel("Independent Variable (X)")
plt.ylabel("Dependent Variable (Y)")
plt.title("Univariate Linear Regression")
plt.legend()
plt.grid(True)
plt.show()
```

## Output:

<img width="1782" height="450" alt="image" src="https://github.com/user-attachments/assets/7c4e6f10-37bc-4419-adb3-01d0fe692337" />

<img width="1146" height="627" alt="image" src="https://github.com/user-attachments/assets/b55a7c39-254a-4160-bd58-64db72d0bd63" />

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
