# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
### step 1: Start the program
### step 2: import the required libraries and read the number of equations and the augmented matrix
### step 3: Apply Gaussian Elimination to convert the matrix into an upper triangular matrix then use back substitution to find the values of the unknowns
### step 4: Display the solution and stop the program 

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: ESAIYA E 
RegisterNumber:26014140
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
  for j in range(n+1):
     a[i][j]=float(input())
for i in range(n):
  if a[i][i]==0.0:
    sys.exit
  for j in range(i+1,n):
    ratio=a[j][i]/a[i][i]
    for k in range(n+1):
      a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
   x[i]=a[i][n]
   for j in range(i+1,n):
      x[i]=x[i]-a[i][j]*x[j]
   x[i]=x[i]/a[i][i]
for i in range(n):
   print('X%d = %0.2f' % (i,x[i]), end=' ') 
*/
```

## Output:
![gaussian elimination]()

<img width="832" height="881" alt="Screenshot 2026-10-16 225044" src="https://github.com/user-attachments/assets/8397aecb-dcda-46bc-a7ae-2bbeef948727" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

