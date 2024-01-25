---
tags:
  - Linear-algebra
---
A process to transform any [[basis]] into an [[orthonormal basis]].

A *basis* (composed by [[linear independence|linear independent]] vectors) $\displaystyle \large v$ can be defined as:
$$\displaystyle \Huge \begin{eqnarray} 
v &=& \{v_1, v_2, \dots,v_n\}
\end{eqnarray}$$

*Gram-Schmidt* normalises it like this:
$$\displaystyle \Huge \begin{eqnarray} 
e_1 &=& \dfrac{v_1}{|v1|} \\\\

u_2 &=& v_2 - (v_2 \cdot e_1)*e_1 \\
e_2 &=& \dfrac{u_2}{|u_2|} \\\\

u_3 &=& v_3 - (v_3 \cdot e_1)*e_1 - (v_3 \cdot e_2)*e_2\\
e_3 &=& \dfrac{u_3}{|u_3|} \\\\

\dots \\\\

u_n &=& v_n - \sum_{i=0}^{n-1}(v_n \cdot e_i)*e_i\\
e_n &=& \dfrac{u_n}{|u_n|} \\\\
\end{eqnarray}$$

>[!info] Explanation
>1. The first arbitrary vector, $\displaystyle \large e_1$, is just its original form, normalised.
>
>2. The second arbitrary vector, $\displaystyle \large e_2$, is the perpendicular part of $\displaystyle \large v_2$ in relation to $\displaystyle \large e_1$. We can use [[Vector projection]] to find it
>![[Pasted image 20240125150034.png|300]]
>$$\displaystyle \Huge \begin{eqnarray} 
>v_2 &=& proj_{e_1}v_2 + u_2\\
>&\text{so}& \\
>u_2 &=& v_2 - proj_{e_1}v_2  \\
>u_2 &=& v_2 - (v_2 \cdot e_1)*e_1
>\end{eqnarray}$$
>Then we have to [[unit vector|normalise]] the vector $\displaystyle \large u_2$
>$$\displaystyle \Huge \begin{eqnarray} 
>e_2 &=& \dfrac{u_2}{|u_2|}
>\end{eqnarray}$$
>
>3. From now one, we just need to get the projections of each $\displaystyle \large v_n$ onto each $\displaystyle \large e_i$ already calculated ($\displaystyle \large i < n$), to find the perpendicular vector of each one of them:
>$$\displaystyle \Huge \begin{eqnarray} 
>u_n &=& v_n - \sum_{i=0}^{n-1}proj_{e_i}v_n \\
>u_n &=& v_n - \sum_{i=0}^{n-1}(v_n \cdot e_i)*e_i\\
>\end{eqnarray}$$
>Then [[unit vector|normalise]] the vector $\displaystyle \large u_n$
>$$\displaystyle \Huge \begin{eqnarray} 
>e_n &=& \dfrac{u_n}{|u_n|}
>\end{eqnarray}$$
