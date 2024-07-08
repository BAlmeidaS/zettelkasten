---
tags:
  - deep-learning
---
This is heavily in many papers. To simplify notation, when you have many *Weights* matrix in a model, *instead of given different names to them*, **you may call all of them $\displaystyle \large W$** and *do this notation trick of stacking inputs* with the notation $\displaystyle \large [a, b, \dots]$:


$$\displaystyle \Huge \begin{eqnarray} 
f(x,y) = W_1*x + W_2*y + b
\end{eqnarray}$$

might be converted to:
$$\displaystyle \Huge \begin{eqnarray} 
f(x,y) = W*[x, y] + b
\end{eqnarray}$$


So $\displaystyle \large W$ is the *horizontal stack of $\displaystyle \large W_1$ and $\displaystyle \large W_2$* :
![[Pasted image 20240708170322.png|200]]

And $\displaystyle \large [x, y]$ is the *vertical stack* of $\displaystyle \large x$ and $\displaystyle \large y$:
![[Pasted image 20240708141255.png|200]]
