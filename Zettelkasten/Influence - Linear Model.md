---
tags:
  - Statistics
---
One of the commonest reasons for a lack of [[Degree of Fit - Linear Regression]] is through the existence of [[Outliers]] in the data.

We have to understand if it is an *outlier because of misspecification of the model* (not because there is something wrong with the data).

Points that are *highly infruential* *bring the [[Regression Analysis|Linear Model]] close to them*, so you cannot rely on residuals. This points are *outliers that demand further investigation*

The measure of leverage is:
$$\displaystyle \Huge h_i = \dfrac{1}{n} + \dfrac{(x_i - \bar{x})^2}{\sum(x_i-\bar{x})^2}$$

A thumb rule is that, **A point is highly influential if:**
$$\displaystyle \Huge h_i \gt \dfrac{2p}{n}$$

being $\displaystyle \large n$ the number of datapoints, and $\displaystyle \large p$  the number of parameters in the model (counting with intercept)
> [!R lang]
> In `r` you can get which point is highly influential using
> ```R
> model <- lm(...)
> influence.measures(model)
> ```
> The col *inf* will mark with an asterisk \* the highly influential points

