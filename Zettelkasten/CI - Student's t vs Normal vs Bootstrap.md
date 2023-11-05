---
tags:
  - Statistics
---
Remember that, for small-sample confidence intervals, using [[Values of Student's T|Values of Student's T]], the sample size ($\displaystyle \large n$) enters the equation twice:
1. as the denominator in the formula for [[Standard Error of the mean]]
2. as a determinant of the quantile of the t distribution `qt(probability, n-1)`, being n-1 the degrees of freedom.

That is the reason that difference between the Normal and the [[Values of Student's T]] gets bigger as sample size gets smaller.

What is the best?

*[[Bootstrap]] because it makes fewer assumptions*, since it is a non-parametric method. This is even more noticeable when you have skewed data.