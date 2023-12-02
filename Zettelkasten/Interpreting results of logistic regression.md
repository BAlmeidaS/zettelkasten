---
tags:
  - Statistics
---
The *coefficients* obtained from the [[logistic regression]] are *the change in the [[Log Odds]] of the outcome for one unit increase in the [[Explanatory variable]]*.

Using `R` we create the [[logistic function]] (`logistic_model`) and we have the coefficients. 

>[!example]
> ![[Pasted image 20231202155310.png]]
>- for every one unit change for distance the log odds of making the shot decrease by 0.8667
>- wide orientation, versus narrow orientation, changes the log odds of making the shot by 0.4708

Using `R` we can calculate the [[Odds Ratio]] removing the *log* of the [[log odds]] of the coeficients:
```R
exp(coef(logistic_model))
```


>[!example]
>![[Pasted image 20231202160321.png]]
>- For a one unit increase in distance, the odds of making the shot (versus not making the shot) increase by a factor of 0.42. In other words they decrease.
>- The odds (or likelihood) of making the shot (versus not making the shot) increase by a factor of 1.6 when the orientation is wide
