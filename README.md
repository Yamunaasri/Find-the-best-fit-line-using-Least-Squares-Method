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
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: T.S. Yamunaasri
RegisterNumber:  212222240117
*/

import numpy as np
import matplotlib.pyplot as plt

x=np.array(eval(input()))
y=np.array(eval(input()))

x_m=np.mean(x)
y_m=np.mean(y)
num,denom=0,0

for i in range(len(x)):
  num+=(x[i]-x_m)*(y[i]-y_m)
  denom+=(x[i]-x_m)**2

m=num/denom     #slope
b=y_m-(m*(x_m))     #intercept

print("slope:",m,"intercept=",b)
#line eq
y_predict=m*x+b
print("y prediction=",y_predict)

#plotting the graph
plt.scatter(x,y)
plt.plot(x,y_predict,color='red')
plt.show

a=m*3+b
print("when x=3:",a)
```
## Output:
![introtomlexp1 - Copy - Copy](https://user-images.githubusercontent.com/115707860/225343605-34cbd9b4-5469-48eb-ba0b-d439f2b06b22.png)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
