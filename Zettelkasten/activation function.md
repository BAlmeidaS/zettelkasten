---
tags:
  - deep-learning
---
*Activation function* is a mathematical function applied in a neuron that returns "how much" that function is activated (considering the inputs and outputs). 

It plays an important role in deep learning because they introduce the *non-linear* behaviour to [[Neural networks]].

Activation functions must be:
- **Non-linear**: otherwise they could collapse in a unique linear function
- [[differentiable]]: because via [[back-propagation]] their gradients will be calculated 

Some examples of activation functions are:
- [[Sigmoid function]]
- [[Hyperbolic Tangent function]]
- [[ReLU function]]
- [[Leaky ReLU]]
- [[softmax function]]