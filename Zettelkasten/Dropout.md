---
tags:
  - deep-learning
aliases:
  - inverted dropout
---
a [[Regularisation]] technique applied on *deep learning*.

In its most common form (often called _inverted dropout_), the usual statement is:
- **Training phase:** Each neuron's output is "dropped" (set to zero) with probability $\displaystyle \large p$. If it is _not_ dropped, it is rescaled (multiplied) by $\displaystyle \large \dfrac{1}{1-p}$ .
- **Test (inference) phase:** No neuron is dropped—i.e., you use the full network—and **no further scaling** is applied.

That means in practice, if you use inverted dropout (as is typical in PyTorch, TensorFlow, etc.), you **do not** multiply the weights or outputs by $\displaystyle \large (1-p)$ at test time. The scaling by $\displaystyle \large \dfrac{1}{1-p}$ is already accounted for during training, so nothing extra is done during inference.


### the naive (original) dropout scaling

There is a slightly different older or “naïve” version of dropout in which:
- **Training phase:** You drop out each neuron’s output with probability $\displaystyle \large p$ _without_ the $\displaystyle \large \dfrac{1}{1-p}$ scaling.
- **Test phase:** You then multiply the neuron’s weights (or activations) by $\displaystyle \large 1-p$.

This approach keeps the overall activation magnitude consistent between training and test, but *it is less popular in many modern deep-learning frameworks because it makes the test-time code more complicated*.

In contrast, *inverted dropout* “pushes” that consistency to training time and leaves test-time inference simpler.
