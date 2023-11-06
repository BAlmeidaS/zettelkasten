---
tags:
  - Statistics
aliases:
  - Q-Q plot
---
*Q-Q plot* is a simple test of [[Normal Distribution|normality]].

If the sample is *normally distributed* then the line will be straight. Departures from normality show up as various sorts of non-linear functions (s-shapes, banana shapes).
![[Pasted image 20231106175944.png|500]]

The functions you need to remember on `R` are `qqnorm` and `qqline`