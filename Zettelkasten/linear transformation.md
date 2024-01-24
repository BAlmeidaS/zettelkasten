---
tags:
  - Linear-algebra
---
*Linear transformation* is a **function** that transform any **input vector** into an **output vector**. Thus, it changes the space.
![[Pasted image 20240124172936.png|400]]

*Linear transformations* have 2 special properties, that must be kept to be considered *linear*:
- lines must remain lines (after the transformation) - *"grid lines remain parallel and evenly spaced"*
- Origin remains fixed

The *algebraic definition* of a linear transformation, being $\displaystyle \large L$ a linear transformation:
1. $\displaystyle \large L$ preserves sums
$$\displaystyle \Huge \begin{eqnarray} 
\displaystyle \large L(\vec{v} + \vec{w}) = L(\vec{v}) + L(\vec{w})
\end{eqnarray}$$
2. $\displaystyle \large L$ preserves scaling
$$\displaystyle \Huge \begin{eqnarray} 
\displaystyle \large L(s\vec{v}) = sL(\vec{v})
\end{eqnarray}$$

This is a linear transformation:
![[Pasted image 20240124173439.png|400]]

While this transformation **is not**:
![[Pasted image 20240124173537.png|300]]

**[[Matrix]] can be used to represent linear transformations!**

A matrix that makes a linear transformation in a space of *$\displaystyle \large n$ dimensions* has $\displaystyle \large n\times n$  *shape*.
The first column is to where $\displaystyle \large \hat{i}$ is going (being $\displaystyle \large \hat{i}$ a [[unit vector]] that points towards x-axis)
The second column is to where $\displaystyle \large \hat{j}$ is going (being $\displaystyle \large \hat{j}$ a [[unit vector]] that points towards y-axis)
...

![[Pasted image 20240124174303.png|400]]

And the matrix can be used as a function to transform input vectors
$$\displaystyle \Huge \begin{eqnarray} 
A * \vec{x} &=& \vec{y} \\\\
\text{for instance,} \\
\begin{bmatrix} 3 & 1 \\ 1 & 2\end{bmatrix}
\begin{bmatrix} -1 \\ 2\end{bmatrix}
&=&
\begin{bmatrix} -1 \\ 3\end{bmatrix}

\end{eqnarray}$$
![[Pasted image 20240124174640.png|500]]