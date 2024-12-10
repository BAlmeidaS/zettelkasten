---
tags:
  - deep-learning
---
A common problem on deep learning, occurs when [[gradient]] becomes very large as they are propagated back through the network during [[back-propagation]].

*This makes difficult to converge*, leading to unpredictable and wrong paths on the loss function.

*Usually this problem is easily spot* since the parameters will be set to a huge number or even NaN and can be solved by [[Gradient Clipping]]

>[!note]
>In deep learning, error gradients can accumulate during an update and result in very large gradients. These in turn result in large updates to the network wrights and on an unstable network. At an extreme, the values of weights can become so large as to overflow and result and NaN values 

---
see also [[vanishing gradient problem]]