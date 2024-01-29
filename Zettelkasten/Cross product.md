---
tags:
  - Linear-algebra
---
We define the *cross product* between the [[vector]] $\displaystyle \large \vec{a}$ and [[vector]] $\displaystyle \large \vec{b}$ as the [[vector]] $\displaystyle \large \vec{c}$
$$\displaystyle \Huge \begin{eqnarray} 
\vec{a} \times  \vec{b} = \vec{c}
\end{eqnarray}$$
- cross product *returns a vector* (above $\displaystyle \large \vec{c}$). Moreover, **$\displaystyle \large \vec{c}$ is perpendicular to $\displaystyle \large \vec{a}$ and $\displaystyle \large \vec{b}$**
- cross product *only works in 3 dimensions*
- cross product measures *how much two vectors point in **different directions**

![[Pasted image 20240129161821.png]]

(it follows the right hand rule)
![[Pasted image 20240129161906.png|180]]

*It is calculated as follow:*
$$\displaystyle \Huge \begin{eqnarray} 
\vec{c} &=& det\left(\begin{bmatrix} 
\hat i & \hat j & \hat k \\ 
a_1 & a_2 & a_3 \\
b_1 & b_2 & b_3 \\
\end{bmatrix}\right)\\\\

\vec{c} &=& 
(a_2b_3-a_3b_2)\hat i +
(a_3b_1-a_1b_3)\hat j +
(a_1b_2-a_2b_1)\hat k \\
&\text{or}& \\
\vec{c} &=& \begin{bmatrix}  
a_2b_3-a_3b_2\\
a_3b_1-a_1b_3\\
a_1b_2-a_2b_1
\end{bmatrix} 
\end{eqnarray}$$
