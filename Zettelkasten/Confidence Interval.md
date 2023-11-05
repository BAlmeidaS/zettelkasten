---
tags:
  - Statistics
---
Shows how likely the [[Average|mean]] would fall if the sampling were to be repeated.

$$\displaystyle \Huge confidence\ interval \propto unreliability \propto \sqrt{\dfrac{s^2}{n}} $$

*The higher the confidence, the wider the interval*. If you want to be 100% sure the interval is infinite.

---
Let's say that we want to calculate a 95% confidence interval for a small sample(n<30), so we can use [[Values of Student's T]]:
$$\displaystyle \Huge \begin{eqnarray} 
\text{confidence interval} &=& \text{t-value} * \text{standard error}  \\
CI_{95\%} &=& t_{(\alpha=0.025, d.f.=9)} \sqrt{\dfrac{s^2}{n}}\\
\end{eqnarray}$$

with this example of 95% of confidence interval,
$$\displaystyle \Huge mean = mean \pm CI_{95\%}\ (95\%\ CI, n=10) $$