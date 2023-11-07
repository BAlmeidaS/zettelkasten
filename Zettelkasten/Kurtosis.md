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

*Positive kurtosis* is a *pointy distribution* (Leptokurtic)
*Negative kurtosis* is a *flat-topped distribution* (Platykurti)

The approximate Standard Error of kurtosis is:
$$\displaystyle \Huge SE_{\gamma_2} = \sqrt{\dfrac{24}{n}}$$

---

We use $\displaystyle \large SE_{\gamma_2}$ to validate if the distribution is or is not a normal, using [[Student's t test|t test]]:

if $\displaystyle \large \left|\dfrac{\gamma_2}{SE_{\gamma_2}}\right| < 2$ ,(this 2 came from the [[Student's t = 2 rule of thumb]]), so this distribution is smilar to a normal. if it is bigger we know that it is not close to a gaussian and we must see the signal of $\displaystyle \large \gamma_2$ to know if it is Leptokurtic or Platykurti distributions.