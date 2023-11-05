---
tags:
  - Statistics
---
Values of student's t can be used to calculate [[Confidence Interval]].

The values of Student's t associated with different levels of confidence are available under the function `qt` in R.
$$\displaystyle \Huge qt(probability, degrees\_of\_freedom)$$

For instance,
```R
qt(0.975,9)
[1] 2.262157
```

Which means 2.26 standard errors to the right.

*Values of student's t are numbers of standard errors to be expected with specified probability and for a given number of degrees of freedom.*
