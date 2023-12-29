# Algorithm for QR Decomposition
### Name: Anbuselvan.S
### Reference No: 23005959
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Intialize the matrix Q and u
2.	The vector u and e is given by

    ![eqn1](./ex4.jpg)

    ![eqn2](./ex6.jpg)

    ![eqn3](./ex3.jpg)

3.	Obtain the Q matrix   
    ![eqn4](./ex1.jpg)
4.	Construct the upper triangular matrix R
    ![eqn5](./ex2.jpg)

## Program:
### Gram-Schmidt Method
```
Program to QR decomposition using the Gram-Schmidt method
Developed by: Anbuselvan.S
RegisterNumber: 23005959
import numpy as np
def QR_Decomposition(A):
    n,m=A.shape
    q=np.empty((n,n))
    u=np.empty((n,n))
    u[:,0]=A[:,0]
    q[:,0]=A[:,0]/np.linalg.norm(u[:,0])
    for i in range(1,n):
        u[:,i]=A[:,i]
        for j in range(i):
            u[:,i]-=(a[:,i]@q[:,j])*q[:,j]
        q[:,i]=u[:,i]/np.linalg.norm([u[:,i]])
    r=np.zeros((n,m))
    for i in range(n):
        for j in range(i,m):
            r[i,j]=a[:,j]@q[:,i]
    print(q)
    print(r)
a = np.array(eval(input()))
QR_Decomposition(a)
```

## Output
![image](https://github.com/anbuselvan1519/QRdecomposition/assets/139841744/78eafcf9-9fce-4b07-b409-053c524e46fa)

## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
