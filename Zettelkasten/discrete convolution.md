---
tags:
  - math
---
The idea here is understanding [[Convolution]] but only with discrete cases

The convolution of two [[sequence]] $\displaystyle \large (a_i)$ and $\displaystyle \large (b_i)$ is defined as:
$$\displaystyle \Huge \begin{eqnarray} 
(a*b)_n = \sum\limits_{\substack{i,j \\[3pt] i+j = n}} a_i\cdot b_i
\end{eqnarray}$$

>[!example]
>Considering the two [[sequence]] with 6 elements:
>$$\displaystyle \Huge \begin{eqnarray} 
>(a_1, a_2, a_3, a_4, a_5, a_6)
>\\
>(b_1, b_2, b_3, b_4, b_5, b_6)
>\end{eqnarray}$$
>The convolution of $\displaystyle \large a$ and $\displaystyle \large b$ results in the following sequence:
>$$\displaystyle \Huge \begin{align} 
>(\\
>&a_1\cdot b_1,\\
>&a_1\cdot b_2 + a_2\cdot b_1,\\
>&a_1\cdot b_3 + a_2\cdot b_2 + a_3\cdot b_1,\\
>&a_1\cdot b_4 + a_2\cdot b_3 + a_3\cdot b_2 + a_4\cdot b_1,\\
>&a_1\cdot b_5 + a_2\cdot b_4 + a_3\cdot b_3 + a_4\cdot b_2 + a_5\cdot b_1,\\
>&a_1\cdot b_6 + a_2\cdot b_5 + a_3\cdot b_4 + a_4\cdot b_3 + a_5\cdot b_2 + a_6\cdot b_1,\\
>&a_2\cdot b_6 + a_3\cdot b_5 + a_4\cdot b_4 + a_5\cdot b_3 + a_6\cdot b_2,\\
>&a_3\cdot b_6 + a_4\cdot b_5 + a_5\cdot b_4 + a_6\cdot b_3,\\
>&a_4\cdot b_6 + a_5\cdot b_5 + a_6\cdot b_4,\\
>&a_5\cdot b_6 + a_6\cdot b_5,\\
>&a_6\cdot b_6\\
>)
>\end{align}$$

The operation can be described as *rolling* the *opposite sequence* from *left to right* on the first sequence. Hopefully is possible to see this on the example above. Since $\displaystyle \large a_1$ start multiplying $\displaystyle \large b_1$ rather than $\displaystyle \large b_6$.

The discrete case is useful to calculate *moving averages*.

>[!example]
>Example of a *moving average using convolution* of *five items* being calculated in a list of values
>![[Peek 2024-07-10 20-03.gif]]


Both *numpy* and *scipy* implement convolution, however scipy has a *way faster implementation* called [[fftconvolve]]

![[Pasted image 20240710203132.png]]