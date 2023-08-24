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
Developed by: AUGUSTINE J
RegisterNumber:212222240015
*/
```
```
# least square method

import matplotlib.pyplot as plt
x=[5,6,3,2,6,7,1,2]
y=[2,3,6,5,8,3,5,8]
plt.scatter(x,y);
plt.plot(x,y)
plt.show()

import numpy as np
import matplotlib.pyplot as plt

# assign input

X=np.array([0,1,2,3,4,5,6,7,8,9])
Y=np.array([1,3,2,5,7,8,8,9,10,12])

# mean values of input

X_mean=np.mean(X)
print(X_mean)
Y_mean=np.mean(Y)
print(Y_mean)

num=0
denum=0

for i in range (len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denum+=(X[i]-X_mean)**2
  
# find m

m=num/denum
print(m)

# find b

b=Y_mean-m*X_mean
print(b)

# find Y_pred

Y_pred=m*X+b
print(Y_pred)

# plot graph

plt.scatter(X,Y)
plt.plot(X,Y_pred,color='green')
plt.show()  
*/
```

## Output:
![best fit line](sam.png)
![image](https://github.com/Augustine0306/Find-the-best-fit-line-using-Least-Squares-Method/assets/119404460/c8769e4a-94e8-45a5-a9ef-3f81e7011433)
![image](https://github.com/Augustine0306/Find-the-best-fit-line-using-Least-Squares-Method/assets/119404460/3148b825-c7c8-43d9-8fd6-a750391aee14)
![image](https://github.com/Augustine0306/Find-the-best-fit-line-using-Least-Squares-Method/assets/119404460/1a04c3b6-4c79-4be9-bd0f-9e452c868430)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
