# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```python
import numpy as np
import matplotlib.pyplot as plt

x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])

plt.scatter(x,y)
plt.show()

xmean = np.mean(x)
ymean = np.mean(y)

num = 0
den = 0

for i in range(len(x)):
    num += (x[i]-xmean)*(y[i]-ymean)
    den += (x[i]-xmean)**2

m = num/den
b = ymean-m*xmean
print(m,b)

ypred = m*x + b
print(ypred)

plt.scatter(x,y,color='red')
plt.plot(x,ypred, color='blue')
plt.show()




```
## Output
![image](https://github.com/user-attachments/assets/5e0c03a5-4176-4877-b6e9-a91cf6daa8d2)

</br>1.1696969696969697 1.2363636363636363
</br>[ 1.23636364  2.40606061  3.57575758  4.74545455  5.91515152  7.08484848
  8.25454545  9.42424242 10.59393939 11.76363636]
  
</br>![image](https://github.com/user-attachments/assets/ff169a7f-877b-415e-b377-eebddc5fc301)

![image](https://github.com/user-attachments/assets/cc91b9ec-fd8c-48d0-b67c-2652e3f56ef8)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
