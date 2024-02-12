---
tags:
  - deep-learning
---
Fundamentally, neural networks are just a [[vector-valued function]] $\displaystyle \large \mathbb{R}^n \rightarrow \mathbb{R}^m$:
$$\displaystyle \Huge \begin{eqnarray} 
\boldsymbol{y} = f(\boldsymbol{x})
\end{eqnarray}$$
![[Pasted image 20240202155332.png|300]]

It is composed of [[neurons]], and this can be formulated as,
- $\displaystyle \large a$: activity
- $\displaystyle \large w$: weight
- $\displaystyle \large b$: bias
- $\displaystyle \large \sigma$: [[activation function]]

>[!note] The simplest neural network
>![[Pasted image 20240202155507.png|250]]
>$$\displaystyle \Huge \begin{eqnarray} 
>a^{(1)} &=& \sigma(wa^{(0)} + b)
>\end{eqnarray}$$

>[!note] The general case with two layers
>![[Pasted image 20240202160317.png|200]]
being the *bold symbols* the [[vector]] form of them, and the *bold and capitalize* the [[matrix]] form.
>And the use of [[dot product]]:
>$$\displaystyle \Huge \begin{eqnarray} 
>\boldsymbol{a}^{(1)} &=& \sigma(\boldsymbol{W}^{(1)} \cdot \boldsymbol{a}^{(0)} + \boldsymbol{b}^{(1)})
>\end{eqnarray}$$
>![[Pasted image 20240202160624.png]]

>[!important] the general case with many layers
>![[Pasted image 20240202160810.png|200]]
>$$\displaystyle \Huge \begin{eqnarray} 
>\boldsymbol{a}^{(L)} &=& \sigma(\boldsymbol{W}^{(L)} \cdot \boldsymbol{a}^{(L-1)} + \boldsymbol{b}^{(L)})
>\end{eqnarray}$$

