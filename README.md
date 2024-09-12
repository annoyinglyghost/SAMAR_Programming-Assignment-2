# EXPERIMENT 2
### NUMERICAL PYTHON (NUMPY)
Name: Samar, Mariane Iszley V.
Section: 2ECE-D                                                          
Date Submitted: Sept. 5, 2024 
<br />

## I. Intended Learning Outcomes:
1. To identify the codes and functions incorporated in the Numpy library
2. To be able to apply and use the different codes and functions in creating a Python program using a
Numpy library
<br />

## II. Instructions:
Write a Python script/code in the Jupyter Notebook to do the given problems. You may submit your Jupyter
notebook in the dedicated submission bin.
<br />

## NORMALIZATION PROBLEM: 
Normalization is one of the most basic preprocessing techniques in
data analytics. This involves centering and scaling process. Centering means subtracting the data from the
mean and scaling means dividing with its standard deviation. Mathematically, normalization can be
expressed as: 𝑍 = 𝑋 − 𝑥̅ / 𝜎
<br />
In Python, element-wise mean and element-wise standard deviation can be obtained by using .mean() and
.std() calls. 
<br />
In this problem, create a random 5 x 5 ndarray and store it to variable X. Normalize X. Save your normalized
ndarray as X_normalized.npy
<br />

```python
import numpy as np #importing the numpy library in python to make it easier

X = np.random.random((5,5)) #creating a 5x5 ndarray
mean = X.mean() #normalizing the array
standard = X.std() 
X_normalized = (X-mean) / standard
np.save('X_normalized.np', X_normalized) #saving the normalized ndarray
#printing the original and normalized ndarrays
print("\nOriginal Array:\n", X)
print("\n\nNormalized Array:\n", X_normalized)
```
Output: <br />
![image](https://github.com/annoyinglyghost/Images-2-/blob/main/3.png)

## DIVISIBLE BY 3 PROBLEM: 
Create the following 10 x 10 ndarray
<br />
![image](https://github.com/annoyinglyghost/Images-2-/blob/main/divisible%20by%203.png)
<br />
which are the squares of the first 100 positive integers. <br />
From this ndarray, determine all the elements that are divisible by 3. Save the result as div_by_3.npy

```python
import numpy as np  #importing the numpy library in python to make it easier

A = np.arange(1, 101).reshape(10, 10)**2 #create the 10x10 ndarray with the squares of the first 100 integers
div_by_3 = [A%3 == 0] #formula for getting the elements that are divisible by 3
np.save('div_by_3.npy', div_by_3) #saving the div_by_3.npy
print("\nOriginal Array: \n", A) #printing the original and the elements divisible by 3
print("\n\nThe elements divisible by 3: \n", div_by_3)
```
<br />

Output: <br />
![image](https://github.com/annoyinglyghost/Images-2-/blob/main/6.png)


