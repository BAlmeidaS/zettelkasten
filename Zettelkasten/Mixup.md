---
tags:
  - deep-learning
---
*Mixup* is a [[Data Augmentation]] technique where the *two training examples are linearly combined to create a new example*.

This involves blending both the input features and their labels, helping the model generalise better by learning from mixed data points.

*mixup* extends the training distribution by **assuming** that *the linear interpolation of feature vectors should lead to linear interpolations of the associated targets*

![[Pasted image 20240718150814.png|600]]