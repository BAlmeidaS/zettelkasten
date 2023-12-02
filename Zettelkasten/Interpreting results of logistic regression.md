---
tags:
  - Statistics
---
The *coefficients* obtained from the [[logistic regression]] are *the change in the [[Log Odds]] of the outcome for one unit increase in the [[Explanatory variable]]*.

Using `R` we create the [[logistic function]] (`logistic_model`) and we have the coefficients. 

>[!For instance]For Instance
> ![[Pasted image 20231202155310.png]]
>for every one unit change for distance the log odds of making the shot decrease by 0.8667

Using `R` we can calculate the [[Odds Ratio]] removing the *log* of the [[log odds]] of the coeficients:
```R
exp(coef(logistic_model))
```


>[!For instance]
> ![[Pasted image 20231202155310.png]]
>for every one unit change for distance the log odds of making the shot decrease by 0.8667
