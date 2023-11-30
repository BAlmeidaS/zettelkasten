---
tags:
  - Statistics
aliases:
  - types of simplification over stats models
  - Maximal model
  - Saturated Model
---
In the process over the [[Model Simplification - Model Complexity]] we have the 4 models:

**Null Model**:
	Just one parameter, the overall mean $\displaystyle \large \bar{y}$
	*Fit*: None; SSE = SSY
	[[Degrees of Freedom]]: $\displaystyle \large n - 1$
	[[Degree of Fit - Linear Regression|Explanatory Power]]: none
**Saturated Model**:
	One parameter for every data point
	*Fit*: perfect
	[[Degrees of Freedom]]: none
	[[Degree of Fit - Linear Regression|Explanatory Power]]:  none
**Maximal Model**:
	contain all factor, interaction and covariates that might be of any interest.
	[[Degrees of Freedom]]: $\displaystyle \large n - p - 1$
	[[Degree of Fit - Linear Regression|Explanatory Power]]: depends
**Minimal Adequate Model**:
	A simplified model with $\displaystyle \large 0 \le p^\prime \le p$  parameters
	*Fit*: slightly less than the maximal model
	[[Degrees of Freedom]]: $\displaystyle \large n - p^\prime - 1$
	[[Degree of Fit - Linear Regression|Explanatory Power]]: $\displaystyle \large r^2 = \tfrac{SSR}{SSY}$
 
