---
tags:
  - math
---
A *vector space* (over a [[field]] $\displaystyle \large F$) is a set $\displaystyle \large V$ with *two operations*:

- *Vector Addition*: An operation that takes *two vectors* $\displaystyle \large u, v \in V$ and produces another vector $\displaystyle \large (u+v) \in V$

- *Scalar Multiplication*: An operation that takes a *scalar* $\displaystyle \large a \in F$ (element of the [[field]]) and a vector $\displaystyle \large v \in V$

*Both operations must satisfy a specific collection of [[axioms]]*:
![[Pasted image 20250110172816.png]]

---

*vector spaces* might also be defined using the concept of [[Group]]

A real-valued *vector space* ($\displaystyle \large \mathbb{R}\text{-vector}$)  is a [[set]] $\displaystyle \large V$ with two operations:
$$\displaystyle \Huge \begin{eqnarray} 
+ : V \times V \rightarrow V
\\
\cdot : V \times V \rightarrow V
\end{eqnarray}$$

where:

1. $\displaystyle \large (V, +)$ is an [[Abelian Group]]

2. *distributibity*:
$$\displaystyle \Huge \begin{eqnarray} 
(a)&\ \lambda \cdot (x+y) &=&\ \lambda \cdot x + \lambda\cdot y, 
&\qquad& \forall \lambda\in\mathbb{R} , x, y \in V
\\
(b)&\ (\lambda + \omega) \cdot x &=&\ \lambda \cdot x + \omega \cdot x,
&\qquad& \forall \lambda,\omega\in\mathbb{R} , xy \in V
\end{eqnarray}$$

3. *associativity* (outer operation)
$$\displaystyle \Huge \begin{eqnarray} 
\lambda \cdot (\omega \cdot x) =
(\lambda \cdot \omega) \cdot x \qquad\forall\lambda,\omega \in \mathbb{R}, x \in V
\end{eqnarray}$$
4. *neutral element* with respect to the outer operation
$$\displaystyle \Huge \begin{eqnarray} 
1\cdot x= x, \qquad\forall x \in V
\end{eqnarray}$$

The element $\displaystyle \large x \in V$ *is called a* [[vector]].

The *neutral element* of $\displaystyle \large (V, +)$ is the zero vector $\displaystyle \large \boldsymbol{0} = [0, ..., 0]^T$.

The *inner operation* $\displaystyle \large +$ is called *vector addition*.

The elements $\displaystyle \large \lambda \in \mathbb{R}$ are called *scalars*.

The *outer operation* $\displaystyle \large \cdot$ is called *multiplication by scalars*.


