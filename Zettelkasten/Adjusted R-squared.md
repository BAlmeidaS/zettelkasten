---
tags:
  - Statistics
---
Using `r` often you will see two types of [[Degree of Fit - Linear Regression|r-squared]].

***Adjusted R-squared** is usually a **better choice** than Multiple for evaluating the overall effectiveness*

- **Definition**: It measures the proportion of variance in the dependent variable that is predictable from the independent variables.
- **Use**: It gives you an overall idea of how well your model explains the variability of the response data.
- **Limitation**: It always increases as you add more [[Explanatory variable|independent variable]] to your model, regardless of whether those [[Explanatory variable|independent variable]] are actually meaningful. This can be misleading, especially with a large number of variables, as it might suggest a better fit than is truly the case.