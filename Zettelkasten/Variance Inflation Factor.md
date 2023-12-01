---
tags:
  - Statistics
aliases:
  - VIF
---
*VIF* helps to detect [[Multi-collinearity]].

- VIF start at 1 and has no upper limit
- *1* means **no correlation** between the variables and any of the other explanatory variables in the model
- between *1 and 5* indicates **moderate** correlation, but usually, don't require an action
- *greater than 5* indicates potentialy high correlation between a given [[Explanatory variable|explanatory variable]] and other [[Explanatory variable|explanatory variables]].

>[!R Lang]
>```R
>model <- lm(...)
>vif(model)
>```