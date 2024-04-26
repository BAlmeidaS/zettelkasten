---
tags:
  - deep-learning
---
The *saturated outputs problem* refers to a situation in neural networks where the [[activation function]] pushes the output of a neuron into extreme values (close to 0 or 1) for a wide range of inputs. 

This can occur with activation functions like [[Sigmoid function]] or [[Hyperbolic Tangent function|tanh]] when the input values are very large or very small. 

When outputs become saturated, it can lead to [[vanishing gradient problem]].