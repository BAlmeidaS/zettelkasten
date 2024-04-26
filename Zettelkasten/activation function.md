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
- [[step function]]
- [[sign function]]
- [[Sigmoid function]]
- [[Hyperbolic Tangent function]]
- [[ReLU function]]
- [[Leaky ReLU]]
- [[softmax function]]

>[!hint] Visual notion of an activation function and common variables
>usually, $\displaystyle \large z$ is the linear combination of the weights with the inputs and the bias
>
>while $\displaystyle \large a$ is the result of the *activation function* applied on z
>![[Pasted image 20240426175305.png|500]]
