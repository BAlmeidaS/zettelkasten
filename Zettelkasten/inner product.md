---
tags:
  - Linear-algebra
---
*Inner product* is a function that is a "generalisation of the [[dot product]]" 
(Linear Algebra done right, 3rd edition, pg 165)

*inner product* of 2 elements is defined as $\displaystyle \large \langle u, v\rangle$  

![[Pasted image 20240119144749.png]]

>[!note] conjugate symmetry
> Every real number equals its [[complex conjulgate]]. Thus if we are dealing with a *real vector space*, then we can *simplify the conjugate symmetry to just symmetry*:
> $$\displaystyle \Huge \begin{eqnarray} 
> \langle u,v \rangle = \langle v, u \rangle, \forall u,v \in V
> \end{eqnarray}$$


---

Imperial College course summarised *additivity and homogeneity* into a single property called *bilinear*.

They define **inner product** as:
- a *mapping* that maps two vectors in a [[vector space]]:
$$\displaystyle \Huge \begin{eqnarray} 
\langle\cdot,\cdot\rangle: V\times V \rightarrow\mathbb{R}
\end{eqnarray}$$
- This *mapping* is:
	- *Bilinear* (linearity in both sides):
$$\displaystyle \Huge \begin{eqnarray} 
	x,y,z \in v, \lambda \in \mathbb{r}
	\\
	\langle\lambda x+z,y\rangle = \lambda\langle x,y \rangle + \langle z, y\rangle
	\\, and \\
	\langle x, \lambda y+z\rangle = \langle \lambda x,y \rangle + \langle x, z \rangle
\end{eqnarray}$$
	- *Positive definite:
$$\displaystyle \Huge \begin{eqnarray} 
\langle x,x\rangle \ge0, 
\langle x,x\rangle = 0 \iff x=0
\end{eqnarray}$$
	- *Symmetry*:
	$$\displaystyle \Huge \begin{eqnarray} 
	\langle x,y\rangle = \langle y,x\rangle
\end{eqnarray}$$

*Many authors, especially on math field **do NOT require bilinear***, rather, they demand only **linearity on the first argument**.

>[!example]
> let's say define one possible inner product in $\displaystyle \large \mathbb{R}^2$:
> $$\displaystyle \Huge \begin{eqnarray} 
> \langle x,y\rangle=x^TIy
> \end{eqnarray}$$
> and this is gives the same result of [[dot product]]
> 
> However, we could define another inner product over $\displaystyle \large \mathbb{R}^2$, that is different from *dot product*, like:
> $$\displaystyle \Huge \begin{eqnarray} 
> \langle x,y\rangle &=& x^TAy, A = \begin{bmatrix} 2 & 1 \\ 1 & 2\end{bmatrix}
> \\
> &=& x^T\begin{bmatrix} 2 & 1 \\ 1 & 2\end{bmatrix}y
> \\
> &=&2x_1y_1+x_2y_1+x_1y_2+2x_2y_2
> \end{eqnarray}$$

Inner products can be extend to other [[vector space]]. like [[inner product of functions]] and [[inner product of random variables]]