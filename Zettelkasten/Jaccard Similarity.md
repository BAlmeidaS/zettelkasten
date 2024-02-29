---
tags:
  - machine-learning
---
A [[Similarity function]] useful to calculate similarity when the datapoints are defined only with [[categorical variable|categorical variables]].

It is defined using the [[Modulus of a vector|norm]] of the *union* and *intersection*:
$$\displaystyle \Huge \begin{eqnarray} 
J(A, B) &=& \dfrac{|A\cap B|}{|A\cup B|}
\end{eqnarray}$$
![[Pasted image 20240229004810.png]]

A [[Similarity function|dissimilarity function]] that works similar to a distance can be derived as
$$\displaystyle \Huge \begin{eqnarray} 
d(A,B) = 1 - J(A, B)
\end{eqnarray}$$

>[!example] Example with binary variables
>With binary variables you just *count* the $\displaystyle \large 1$s.
>![[Pasted image 20240229004931.png|450]]
>So the distance of J(C1, C2) is the intersection set $\displaystyle \large \{item9\}$ and the union set $\displaystyle \large \{item2, item3, item6, item9\}$ :
>$$\displaystyle \Huge \begin{eqnarray} 
>J(C1,C2) &=& \dfrac{|\{i9\}|}{|\{i2, i3, i6, i9\}|} = 0.25\\
>J(C1,C3) &=& 0.5\\
>J(C2,C3) &=& 0
>\end{eqnarray}$$


>[!example] Example with two more complex sets
>$$\displaystyle \Huge \begin{eqnarray} 
>A &=& \{0, 1, 2, 5, 6\}\\
>B &=& \{0, 2, 3, 4, 5, 7, 9\}
>\end{eqnarray}$$
>$$\displaystyle \Huge \begin{eqnarray} 
>J(A,B) &=& \dfrac{A \cap B}{A \cup B} \\
>&=& \dfrac{\{0, 2, 5\}}{\{0, 1, 2, 3, 4, 5, 6, 7, 9\}} \\
>&=& \dfrac{3}{9} \\
>&=& 0.33
>\end{eqnarray}$$
