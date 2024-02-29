---
tags:
  - math
---
A [[distance function]] used on [[Categorical variable]]. Being $\displaystyle \large x$ and $\displaystyle \large y$ two *categorical* objects:
$$\displaystyle \Huge \begin{eqnarray} 
d_{matching} = \sum^d_{i=1} \delta(x_i, y_i)
\end{eqnarray}$$
Being,
$$\displaystyle \Huge \begin{eqnarray} 
\delta(x,y) &=& 
\begin{cases}
0,& \text{if } x = y\\
1,& \text{if } x \ne y
\end{cases}

\end{eqnarray}$$


A possible [[Similarity function|dissimilarity function]] for this case would be:
$$\displaystyle \Huge \begin{eqnarray} 
s_{matching} = \sum^d_{i=1} \dfrac{n_{x_i} + n_{y_i}}{n_{x_i}n_{y_i}}\delta(x_i, y_i)
\end{eqnarray}$$

$\displaystyle \large n_{x_i}$ and $\displaystyle \large n_{y_i}$ are the numbers of objects in the data set that have categories $\displaystyle \large x_i$ and $\displaystyle \large y_i$.

