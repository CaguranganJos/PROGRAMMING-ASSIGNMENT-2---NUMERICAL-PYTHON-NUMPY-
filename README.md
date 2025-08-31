# PROGRAMMING-ASSIGNMENT-2---NUMERICAL-PYTHON-NUMPY-
> deadline: September 3, 2025

## Table of Contents:
  1. Programming Assignment 2.1: Normalization Problem
  2. Programming Assignment 2.2: Divisible by 3 Problem

## Programming Assignment 2.1: Normalization Problem 
Instructions:
Normalization is one of the most basic preprocessing techniques in
data analytics. This involves centering and scaling process. Centering means subtracting the data from the
mean and scaling means dividing with its standard deviation. Mathematically, normalization can be
expressed as:

𝑍 = (𝑋 − 𝑥̅) / 𝜎

In Python, element-wise mean and element-wise standard deviation can be obtained by using .mean() and
.std() calls.

In this problem, create a random 5 x 5 ndarray and store it to variable X. Normalize X. Save your normalized
ndarray as X_normalized.npy

### Entire Code:
```python
import numpy as np

X = np.random.random((5,5)) 
X_mean = X.mean() 
X_std = X.std() 

Z = (X - X_mean)/X_std
np.save("X_normalized.npy", Z)
```
### Step-by-step Thought Process
1. The most important thing to do first is to import the library numpy, as I will be needing its functions, such as arrays in this code.
```python
import numpy as np
```
2. Then, I made a random 5x5 array containing float random values ranging from 0 to 1 and stored it in "X". Before plugging the formula, I need to get the mean and standard deviation element-wise of the array. Thus, I used ".mean()" and ".sts()" to get both values and stored them in X_mean and X_std, respectively.
```python
X = np.random.random((5,5)) 
X_mean = X.mean() 
X_std = X.std() 
```
3. Now that I have stored all the needed data, I have plugged in the formula and stored the value in the variable "Z". After, I save it using "np.save", making the file name "X_normalized.npy". 
```python
Z = (X - X_mean)/X_std
np.save("X_normalized.npy", Z)
```

## Programming Assignment 2.2: Divisible by 3 Problem
Instruction:
Create the following 10 x 10 ndarray. Which are the squares of the first 100 positive integers.
From this ndarray, determine all the elements that are divisible by 3. Save the result as div_by_3.npy

### Entire Code: 
```python
import numpy as np 

num = np.arange(1,101) 
sqr_num = num**2 
num_array = sqr_num.reshape(10,10) 
div_by_3 = num_array % 3 == 0 
result = num_array[div_by_3]

np.save("div_by_3.npy", result) 
```

### Step-by-step Thought Process
1. First, is to import the library numpy as np, which we will be needing its functions in this code.
```python
import numpy as np 
```


## Author:
Name: Cagurangan, Jos Kendrick L.

Section: 2ECE - B

