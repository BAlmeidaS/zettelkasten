---
tags:
  - deep-learning
---
Dying ReLU Problem is the problem with [[ReLU function|ReLU]] and the fact that its gradient is zero on negative values. This is the main reason that [[Leaky ReLU]] exists.

---

For example, a large gradient flowing through a ReLU neuron could cause the weights to update in such a way that the neuron will never activate on any datapoint again. 

If this happens, then the gradient flowing through the unit will forever be zero from that point on. That is, the ReLU units can irreversibly die during training since they can get knocked off the data manifold.

For example, you may find that as much as 40% of your network can be "dead" (i.e. neurons that never activate across the entire training dataset) if the learning rate is set too high. With a proper setting of the learning rate this is less frequently an issue.