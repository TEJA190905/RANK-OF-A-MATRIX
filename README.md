# RANK-OF-A-MATRIX
## Aim:
To write a python program to find the rank of a matrix
## Equipment’s required:
1. 	Hardware – PCs
2. 	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step 1: 
### Step 2: 
### Step 3: Using the np.linalg.matrix_rank(), we can find the rank of the given matrix.
### Step 4: 
## Program:
```
Developed by: M THEJESWARAN
Reg no:212223240168

import numpy as np

def find_rank(matrix):

    matrix = np.array(matrix, dtype=float)

    for i in range(min(matrix.shape)):
        # Find the pivot element
        pivot_row = np.argmax(np.abs(matrix[i:, i])) + i
        matrix[[i, pivot_row]] = matrix[[pivot_row, i]]
        matrix[i] /= matrix[i, i]

        for j in range(i + 1, matrix.shape[0]):
            matrix[j] -= matrix[j, i] * matrix[i]

  
    rank = np.count_nonzero(np.sum(np.abs(matrix), axis=1))
    return rank


matrix = [[5, -3, -10], [2, 2, -3], [-3, -1, 5]]


rank = find_rank(matrix)
print(rank)

```
## Output:
![Screenshot (3)](https://github.com/TEJA190905/RANK-OF-A-MATRIX/assets/167788543/2948bf96-ebdf-46dc-947d-22cdddad8bb5)

## Result:
Thus the rank for the given matrix is successfully solved by  using a python program.

