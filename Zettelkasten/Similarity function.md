---
tags:
  - math
aliases:
  - similarity coefficient
  - dissimilarity function
  - dissimilarity
  - similarity
---
*Similarity function* $\displaystyle \large s(x, y)$ is a function that indicates *the strength of the relationship between two data points $\displaystyle \large x$ and $\displaystyle \large y$*.

It follows the following properties:
$$\displaystyle \Huge \begin{eqnarray} 
& & 0 \le s(x,y) \le 1 \\
& & s(x,x) = 1 \\
\text{(symmetry) }& & s(x,y) = s(y,x)
\end{eqnarray}$$

$\displaystyle \large s(x,y)$ is known as *similarity coefficient*.

$\displaystyle \large d(x,y)$ is defined as *dissimilarity coefficient* and is defined as $\displaystyle \large d(x,y) = 1 - s(x,y)$. It has a close relation with a [[distance function]], but it is *not a distance function* because it has *softer properties*.
