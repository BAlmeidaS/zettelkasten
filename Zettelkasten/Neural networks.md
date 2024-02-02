---
tags:
  - deep-learning
---
Fundamentally, neural networks are just a [[vector-valued function]] $\displaystyle \large \mathbb{R}^n \rightarrow \mathbb{R}^m$:
$$\displaystyle \Huge \begin{eqnarray} 
\boldsymbol{y} = f(\boldsymbol{x})
\end{eqnarray}$$
![[Pasted image 20240202155332.png|300]]

The simplest neural network will be:
![[Pasted image 20240202155507.png|300]]
$$\displaystyle \Huge \begin{eqnarray} 
a^{(1)} &=& \sigma(wa^{(0)} + b)
\end{eqnarray}$$
Being,
- $\displaystyle \large a$: activity
- $\displaystyle \large w$: weight
- $\displaystyle \large b$: bias
- $\displaystyle \large \sigma$: [[activation function]]

