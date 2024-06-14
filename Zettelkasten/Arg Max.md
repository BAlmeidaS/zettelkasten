---
tags:
  - math
---
In *mathematics* (tho the same definition is applied in Python) the *arg max* is the arguments of the maxima.

Given a [[set]] $\displaystyle \large X$, an *ordered set* $\displaystyle \large Y$, and a function $\displaystyle \large f: X \rightarrow Y$ :
$$\displaystyle \Huge \begin{eqnarray} 
\arg\max_S f &=& \arg\max_{x\in S}f(x) \\
&=& \{x \in S: f(s)\le f(x), \forall s \in S\}

\end{eqnarray}$$

>[!tip] in python
>```python
>import numpy as np
>l = [3, 1, 7, 2]
>np.argmax(l) # answer: 2
>```
