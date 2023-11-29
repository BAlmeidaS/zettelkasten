---
tags:
  - Statistics
aliases:
  - Generalised linear models
  - GLM
---
When [[Linear Models - Basic assumptions of Response Var|Basic assumptions]] of [[Response variable]] are not true, there are, at least, 4 new *kinds of response variables*:
- [[Response Variable - Count Data|Count data]]
- [[Response Variable - Proportion Data|Proportion]]
- [[Response Variable - Binary Response Data|Binary response data]]
- [[Response Variable - Age-at-death Data|Age-at-death data]]

All of them are handled by a **Generalised linear Model** that allows variance to be non-constant and error non-normally distributed. Though, it still assumes [[Randomisation|random sampling]] and [[independence of errors]].

They all *differ* on the *Constancy of Variance* and *normality of error*.

Variance:
![[Pasted image 20231129125835.png|500]]

A generalised model has three important properties:
- [[GLM - error structure|error structure]]
- [[GLM - linear predictor|linear predictor]]
- [[GLM - link function|link function]]