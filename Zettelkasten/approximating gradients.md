---
tags:
  - Calculus
  - deep-learning
---
The idea is to use the [[gradient]] to find the minimum or the [[Cost function]]. But how can we do it, if we don't have the function analytically? The answer will be *approximate* the [[gradient]] "walking" in all directions

$$\displaystyle \Huge \begin{eqnarray} 
\nabla_f \approx 
\left[
\dfrac{f(x+\Delta x, y, z, \dots)}{\Delta x},
\dfrac{f(x, y+\Delta y, z, \dots)}{\Delta y},
\cdots
\right]
\end{eqnarray}$$
![[Pasted image 20240201200927.png|300]]
_estimating the gradient on the white x_