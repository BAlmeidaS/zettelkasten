---
tags:
  - Statistics
---

When considering complex [[Regression Analysis|Linear Model]] like [[Factorial Experiment]] and [[N-way Anova|Higher-order anova]] we must keep this thumb-rule of **at least 3 data-points per parameter**.

With we intend to use, let's say, 5 [[Explanatory variable]], there will be:
- 10 params of 2-way interactions
- 10 params of 3-way interactions
- 5 params of 4-way interactions
- 1 params of 5-way interaction

Since we must start the [[Model Simplification - Model Complexity]] with the *Maximal model*, so for this case we have $\displaystyle \large 5 \text{ (the plain params)} + 1 \text{ (the intercept)} + 10 + 10 + 5 + 1 = 32$ (honestly should be more because we should apply some [[Transformations - Linear Model|transformation]] on the maximal model, at least the quadratic of each term). So we need, as the minimum of the minimum 96 data points.

If we don't have it, we must start cutting the n-way interactions. Than remove other params. 

It is wise, to go back to start, remove quadratic terms and replace them with n-way interaction adding them until find the best spot, never exceeding the max number of params. If for some reason you cannot add all the 2-way together, add them in random order and create multiple models

*A more conservative rule will say 10 data-points per parameter*