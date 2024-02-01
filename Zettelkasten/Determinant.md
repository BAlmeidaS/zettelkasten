---
tags:
  - Linear-algebra
---
*Determinant* is a number that shows how much an area (or volumes, or hyper-volumes) in the space changed (stretches or squises) after a [[linear transformation]]

![[Pasted image 20240124180441.png|600]]

![[Pasted image 20240124180817.png|600]]

So, what does it means to *be zero*?
- transformations that squishes all the space onto a line (or even a point)

And, what does it means to *be negative*?
- transformations that invert the orientation of space.

*Determinant of a matrix product equals the product of their determinants*:
$$\displaystyle \Huge \begin{eqnarray} 
det(AB)=det(A)det(B)
\end{eqnarray}$$

A simple rule to calculate *determinants* is by [[rule of sarrus]]. But bare in mind that we must appeal to *computational methods* when the matrix is more than $\displaystyle \large 3\times 3$.
