---
tags:
  - computer-languages
---
All codes start with:
```python
import numpy as np
```

### Accessing elements of an array

Given **a** as a matrix
```python
a.shape
# (7, 6)

a[1, 3]
# element of 2st row and 4rd column

a[:, 2]
# array with all elements of the 3rd column

a[1, :]
# array with all elements of the 2nd row
```

### create arrays of 0 or 1s
```python
np.ones((3, 2))
# matrix only with ones with shape 3x2

np.zeros((4, 1))
# matrix only with zeros with shape 3x2
```

### operations are all [[element-wise multiplication|element-wise]]

```python
a = np.array([[4, 1, 2],
              [7, 2, 3]])

b = np.array([[3, 6, 9],
              [7, 8, 2]])

a + b # same logic for -
# [[ 7  7 11]
#  [14 10  5]]

a * b # same logic for /
# [[12  6 18]
#  [49 16  6]]

a ** b
# [[    64      1    512]
#  [823543    256      9]]
```

### operation over axis

if an *aggregation* operation (sum, min, max, ...) runs with axis informed
```python
a = np.array([[2, 1, 3],
              [4, 5, 6]])

np.min(a, axis = 0)
# [2 1 3]

np.min(a, axis = 1)
# [1 4]
```

**Note** that the result has one dimension less! *To keep the same dimension of the input use **keepdims***.

```python
np.min(a, axis=0, keepdims=True)
# [[2 1 3]]
```

### Broadcasting


**Broadcasting** allows you to perform element wise operations on Numpy arrays that are not of the same dimension but can be stratched/duplicated so that they are of the same dimension.

The simplest example for this is when you have to multiply all elements of a Numpy array with a scalar or add a scalar to all elements of the array.

```python
a = np.array([[4, 1, 2],
              [7, 2, 3]])

a * 2
# [[ 8  2  4]
#  [14  4  6]]

c = np.array([5, 3, 4]).reshape((1, 3))
a + c
# [[5 4 6]
#  [8 7 9]]
```

### Matrix multiplication and dot product

The operator is *@*:

```python
a @ b
# dot product between two arrays, a and b

X @ Y
# matrix multiplication between two matrix X and Y
```

### Determinant

given a matrix *A*:
```python
np.linalg.det(A)
```
### Inverse

given a matrix *A*:
```python
np.linalg.inv(A)
```
### Eigenvalues and Eigenvectors

given a matrix *A*:
```python
np.linalg.eig(A)
```

### Convolution
[[Convolution]] are useful way to combine arrays!
```python
np.convolve(A, B)
```

### Inner and Outer product
We would advice you to use [np.outer()](https://numpy.org/doc/stable/reference/generated/numpy.outer.html) and [np.inner()](https://numpy.org/doc/stable/reference/generated/numpy.outer.html) when computing the dot product of 1D arrays.

If $\displaystyle \large X$ is a vector (represented as a 1D array in this course), then `np.inner(X, X)` calculates 
$\displaystyle \large X^T \cdot X$ (the regular inner product) and `np.outer(X, X)` computes $\displaystyle \large X \cdot X^T$.

### reshape an array
If you are performing matrix multiplication between a 2D array and a 1D array, we would advise you to first reshape the 1D array into a 2D array of shape $\displaystyle \large (d,1)$
```python
a = np.arange(6)
# [0, 1, 2, 3, 4, 5]

a.reshape((3, 2))
# [[0, 1, 2],
#  [3, 4, 5]]
```
