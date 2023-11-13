---
tags:
  - Statistics
---
Using `r` often you will see two types of [[Degree of Fit - Linear Regression|r-squared]].

***Multiple R-squared** gives a **Basic** understanding of the model*

- **Definition**: Adjusted R-squared measures the proportion of variance explained by the model, but it adjusts for the number of [[Explanatory variable|independent variable]] in the model.
- **Use**: It is generally considered more reliable for comparing models with different numbers of [[Explanatory variable|independent variable]]. It can decrease if [[Explanatory variable|independent variable]] do not add to the explanatory power of the model, which helps to penalize model complexity.
- **Preference in Multiple Regression**: For multiple regression models, the Adjusted R-squared is often preferred over the Multiple R-squared as it provides a more accurate and conservative estimate of the explanatory power of the model, particularly when you have a large number of [[Explanatory variable|independent variables]].