---
tags:
  - Statistics
---
If we have a [[Normal Distribution]] $\displaystyle \large \boldsymbol{N}(\mu, \sigma)$. The z-score is the amount of standard deviations a particular number $\displaystyle \large x$ is from the mean
$$\displaystyle \Huge \text{z-score}=\dfrac{(x-\mu)}{\sigma}$$

In `R` we find the *z-score* than we run the `pnorm` function to find the probability to have that number or less. If the z-score is positive we do `1-pnorm`, because it is that number or more.

---
For example, if the mean $\displaystyle \large \mu$ of a normal distribution is 100, and the standard deviation $\displaystyle \large \sigma$ is 15, and you have an original number $\displaystyle \large x$ of 115, then the z-score of 115 would be $\displaystyle \large 1$