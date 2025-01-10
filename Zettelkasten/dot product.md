---
tags:
  - Linear-algebra
---
*Dot product* is a scalar number defined as:

$$\displaystyle \Huge \begin{eqnarray} 
r\cdot s &=& \sum r_is_i \\
\end{eqnarray}$$

>[!info] Even more math accurate
> $$\displaystyle \Huge \begin{eqnarray} 
>x^Ty = \sum\limits^N_{i=1} x_iy_i,\ x,y \in \mathbb{R}^N
>\end{eqnarray}$$


>[!example] 
>![[Pasted image 20240118192518.png|450]]
>$$\displaystyle \Huge \begin{eqnarray} 
>r \cdot s &=& r_is_i + r_js_j \\
>&=& 3*-1 + 2*2 \\
>&=& 1
>\end{eqnarray}$$

*dot product* can be also expressed using the angle between the vectors, the [[cosine]] of the angle, and the [[Modulus of a vector|Modulus]]:
![[Pasted image 20240311173822.png|200]]
$$\displaystyle \Huge \begin{eqnarray} 
r\cdot s &=& |r|*|s|*cos(\theta)
\end{eqnarray}$$

so that, *the angle between the vectors can be found using **dot product***:
$$\displaystyle \Huge \begin{eqnarray} 
\cos\theta &=& \dfrac{x^Ty}{\lVert x\rVert *\lVert y\rVert}
\\
\theta &=& \arccos \dfrac{x^Ty}{\lVert x\rVert *\lVert y\rVert}
\end{eqnarray}$$


*dot product* is:
- [[commutative]]
- [[distributive]] 
- [[associative]] **over** scalar multiplication: $\displaystyle \large r\cdot(a*s) = a*(r\cdot s)$
