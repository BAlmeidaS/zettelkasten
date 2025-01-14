---
tags:
  - math
---
[[inner product]] of [[Random Variable|random variables]].

One way to look is understanding *random variables* based on their [[Variance]]. With that in mind, a possible [[inner product]] that we might define is
$$\displaystyle \Huge \begin{eqnarray} 
\langle x,y \rangle = cov[x,y],
\end{eqnarray}$$
since it fits all the requisites of inner product. The *bilinear condition* might be the hardest to proof,
$$\displaystyle \Huge \begin{eqnarray} 
cov(\lambda x+y,z) = \lambda cov[x,z] + cov[y, z]
\end{eqnarray}$$

With this definition the [[Modulus of a vector|length]]  of the random variable might be defined as its [[Standard Deviation|standard deviation]]:
$$\displaystyle \Huge \begin{eqnarray} 
\lvert \lvert x \rvert \rvert = \sqrt{cov[x,x]} = \sqrt{var[x]} = \sigma_x
\end{eqnarray}$$

And the [[angle between vectors|angle]] *between two random variables*:
$$\displaystyle \Huge \begin{eqnarray} 
\cos\theta
&=& \dfrac{\langle x,y \rangle}{\lvert \lvert x \rvert \rvert* \lvert \lvert y \rvert \rvert}
\\\\
&=& \dfrac{cov[x,y]}{\sigma_x*\sigma_y}
\end{eqnarray}$$