---
tags:
  - Statistics
---
A measure of non-normality. It has to do with the fact of the distribution has a *peakyness*, or *flat-toppedness*.

Normal distributions are bell-shaped, *kurtosis* is another type of shape

![[Pasted image 20231106195419.png]]

kurtosis, $\displaystyle \large \gamma_2$ is a measure of how far this distribution is from the gaussian. It is based on the fourth moment of the mean:
$$\displaystyle \Huge \begin{eqnarray} 
kurtosis &=& \gamma_2 = \dfrac{m_4}{s_4} - 3 \\\\

m_4 &=& \dfrac{\sum(y-\bar{y})^4}{n} \\
s_4 &=& var(y)^2 = (s^2)^2 \\
\end{eqnarray}$$

*The $\displaystyle \large -3$ on the formula* appears because the *kurtosis of the Gaussian distribution is 3.*

*Positive kurtosis 