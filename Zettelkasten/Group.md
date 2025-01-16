---
tags:
  - math
---
A *group* is a [[set]] and an **operation** defined over the set.

#### Definition

Consider a set $\displaystyle \large S$ and an operation $\displaystyle \large \otimes: S \rightarrow S$ defined on $\displaystyle \large S$.

Then $\displaystyle \large G := (S, \otimes)$ is a *group* if:
1. *Closure of $\displaystyle \large S$ under*
$$\displaystyle \Huge \begin{eqnarray} 
\otimes: \forall x, y \in S : x \otimes y \in S
\end{eqnarray}$$
2. *Associativity*
$$\displaystyle \Huge \begin{eqnarray} 
\forall x,y,z \in S: (x \otimes y) \otimes z =  x \otimes (y \otimes z)
\end{eqnarray}$$
3. *Neutral element* ("kind of the number 1")
$$\displaystyle \Huge \begin{eqnarray} 
\exists e \in S\ \forall x \in S:x \otimes e = x \text{ and } e \otimes x = x
\end{eqnarray}$$
4. *Inverse element*
$$\displaystyle \Huge \begin{eqnarray} 
\forall x \in S\ \exists y \in S: x \otimes y = e \text{ and } y \otimes x = e
\\\\
\text{often this the inverse element is defined as $x^{-1}$}
\end{eqnarray}$$

>[!example] examples
> - ([[Integer numbers|Integers]]) and $\displaystyle \large +$: $\displaystyle \large (\mathbb{Z}, +)$ is a group
> - [[Natural numbers|Naturals]] and $\displaystyle \large +$: $\displaystyle \large (\mathbb{N}_0, +)$ is *not* a group. It has the neutral element but the inverse element is missing
> - [[Real numbers|Reals]] and $\displaystyle \large +$:  $\displaystyle \large (\mathbb{R^n}, +) \text{ and } (\mathbb{Z}^n, +), n\in \mathbb{N}$ are [[Abelian Group]] if $\displaystyle \large +$ is [[element-wise multiplication|componentwise]]:
> $$\displaystyle \Huge \begin{eqnarray} 
> (x_1,\dots,x_n) +  (y_1,\dots,y_n) = 
> (x_1 + y_1,\dots,x_n + y_n)
> \end{eqnarray}$$
