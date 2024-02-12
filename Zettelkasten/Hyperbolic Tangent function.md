---
tags:
  - deep-learning
aliases:
  - tanh
---
$$\displaystyle \Huge \begin{eqnarray} 
tanh(x) = \dfrac{e^z-e^{-z}}{e^z+e^{-z}}
\end{eqnarray}$$

![[Pasted image 20240212192724.png|300]]

The [[derivative]] of $\displaystyle \large tanh$ is:
$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{d(tanh(x))}{dx}
&=&
\dfrac{d\left(\dfrac{e^x-e^{-x}}{e^x+e^{-x}}\right)}{dx} 
\\
&=&
\dfrac{
(e^x+e^{-x})
(e^x+e^{-x})
}{(e^x+e^{-x})^2} 
- \dfrac{
(e^x-e^{-x})
(e^x-e^{-x})
}{(e^x+e^{-x})^2} 
\\\\
\dfrac{d}{dx}tanh(x)&=&
1- tanh(x)^2
\end{eqnarray}$$
