---
tags:
  - deep-learning
---
The *perceptron* model, it can be understood as the pioneer of the [[Neural networks]] learning models. It consist in a simple models that:
- takes a [[vector]] input, calculate a [[linear combination]] with the *weights*
- if the result is greater or equal a *threshold* (*bias*) then it returns 1 on the *output*, otherwise, returns 0

![[Pasted image 20240310192014.png]]

The process of *learning* in the perceptron is *finding the weights that fit the data the best*. 

*Perceptron* can learn all boolean functions ([[AND]], [[OR]], [[NAND]], [[NOR]]). Unfortunately it cannot represent a [[XOR]], because it is *not linear separable*:
![[Pasted image 20240310192805.png|200]]

This is important because a [[XOR]] can be created using combination of other boolean units (3 NANDs for instance), so we realise that we can *combine layers of perceptrons to learn more complex functions*, and this is the beggining of [[Neural networks]]