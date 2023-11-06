---
tags:
  - Statistics
---
[[Bootstrap]] can be used as a non-parametric [[Hypothesis Test]].

The idea is to answer if some distribution has a [[median]] equal to some $\displaystyle \large \mu_0$. 
So *H0 is $\displaystyle \large \mu$ == $\displaystyle \large \mu_o$ and H1 they differ*

We run Bootstrap and calculate the distribution of the mean of the samples. Then, we check were $\displaystyle \large \mu_0$ falls on the distribution, if it fall inside out [[Confidence Interval]] we *faill to reject H0* (accept H1)