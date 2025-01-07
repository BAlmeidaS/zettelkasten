---
tags:
  - Statistics
---

 *The variance is the square of the [[Standard Deviation]]*, and is a [[measure of dispersion]]
 
*Variance*, on the contrary of [[Sum of squares errors]], it is not super affected by the addition of a new data point. Also it is deeply connected with [[Degrees of Freedom]]:

$$\displaystyle \Huge \begin{eqnarray} 
variance &=& \dfrac{sum\_of\_squares}{degrees\_of\_freedom} \\ \\
variance &=& \sigma^2 = \dfrac{\sum(y-\bar{y})^2}{n}
\end{eqnarray}$$

 $\displaystyle \large \sigma^2$  defines the *population variance*, thus, divided by $\displaystyle \large n$
 $\displaystyle \large s^2$  defines the *sample variance*, thus, divided by $\displaystyle \large n-1$

 Also defined as, given a dataset $\displaystyle \large X$:
 $$\displaystyle \Huge \begin{eqnarray} 
variance = Var[X] &=& \dfrac{1}{N}\sum^N(x_n-\mu)^2 \\
E[X] &=& \mu
\end{eqnarray}$$

---

Another way to understand variance of a dataset $\displaystyle \large D$ is:
$$\displaystyle \Huge \begin{eqnarray} 
Var[D] = E[(D-\mu)(D-\mu)^T]
\end{eqnarray}$$

---
## **Why the right is $\displaystyle \large n-1$ and not $\displaystyle \large n$?**


$$\displaystyle \Huge \begin{eqnarray} 
variance &=& s^2 = \dfrac{\sum(y-\bar{y})^2}{n-1}
\end{eqnarray}$$

---
#### Crawley

The intuitive thing to do would be to divide by the number of numbers, n, to get the mean squared deviation. 

But look at the formula for the sum of squares: $\displaystyle \large \sum (y-\bar{y})^2$. We cannot begin to calculate it until we know the value of the sample mean, $\displaystyle \large \bar{y}$.  And *where do we get the value of $\displaystyle \large \bar{y}$ from?* Do we know it in advance? Can we look it up in tables? No, we need to calculate it from the data. 

The mean value $\displaystyle \large \bar{y}$ is a parameter *estimated from the data, so we lose one degree of freedom* as a result.

Thus, in calculating the mean squared deviation we divide by the degrees of freedom, $\displaystyle \large n-1$, rather than by the sample size, $\displaystyle \large n$. 

In the jargon, this provides us with an unbiased estimate of the variance, because we have taken account of the fact that one parameter was estimated from the data prior to computation.

#### Chatgpt

When calculating the sample variance or standard deviation, one degree of freedom is lost because the mean of the sample is used in the variance calculation.

Here, $\displaystyle \large n-1$ is the degrees of freedom, where $\displaystyle \large n$ is the sample size. The $\displaystyle \large n-1$ comes from the fact that once you have $\displaystyle \large n-1$ data points, the final point must be a certain value to achieve the observed sample mean.