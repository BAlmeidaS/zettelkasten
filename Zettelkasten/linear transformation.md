---
tags:
  - Linear-algebra
---
*Linear transformation* is a **function** that transform any **input vector** into an **output vector**. Thus, it changes the space.
![[Pasted image 20240124172936.png|400]]

*Linear transformations* have **2 special properties**, that must be kept to be considered *linear*:
1. Origin remains fixed
2. lines must remain lines (after the transformation) - *"grid lines remain parallel and evenly spaced"*

>[!note] Algebric definition
> The *algebraic definition* of a linear transformation, being $\displaystyle \large L$ a linear transformation:
>  1. $\displaystyle \large L$ preserves sums
>    $$\displaystyle \Huge \begin{eqnarray} 
>  \displaystyle \large L(\vec{v} + \vec{w}) = L(\vec{v}) + L(\vec{w})
>  \end{eqnarray}$$
>  2. $\displaystyle \large L$ preserves scaling
>  $$\displaystyle \Huge \begin{eqnarray} 
>  \displaystyle \large L(s\vec{v}) = sL(\vec{v})
>  \end{eqnarray}$$

| Linear transformation | **NOT** linear transformation |
| --------------------- | ------------------------- |
| ![[Pasted image 20240124173439.png\|300]]                     | ![[Pasted image 20240124173537.png\|300]]                          |
