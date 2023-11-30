*Logistic regression* fits a [[Sigmoid function]] on the data.

It makes a linear combination of the features:
$$\displaystyle \Huge \begin{eqnarray} 
p(x) &=& \dfrac{1}{1+e^{\tfrac{-(x-\mu)}{s}}} \\ \\

p(x) &=& \dfrac{1}{1+e^{-(\beta_0 + \beta_1x)}} \\

\end{eqnarray}$$

Where,
- $\displaystyle \large \beta_0$ is the **intercept** and $\displaystyle \large \beta_0 = \frac{-\mu}{s}$
- $\displaystyle \large \beta_1$ is the **rate parameter** or the *inverse of the scale* ($\displaystyle \large \beta_1=\frac{1}{s}$)
- $\displaystyle \large \mu$ is the *location parameter* - the midpoint of the curve ($\displaystyle \large p(\mu) = \frac{1}{2}$), also, $\displaystyle \large \mu = \frac{-\beta_0}{\beta_1}$
- $\displaystyle \large s$ is the *scale parameter*, also, $\displaystyle \large s = \frac{1}{\beta_0}$

Finally, the function $\displaystyle \large p(x)$ should be understood as a *probability* to be (or not to be) the output category. Because it *maps any real-valued number to the [0,1] interval*.