---
tags:
  - deep-learning
---
*negative sampling* is an alternative to when you have to calculate a huge [[softmax function|softmax]]. Which means that the below sum on the [[softmax function|softmax]] is so big that the calculation is slow.

So, instead of calculating the softmax on the last layer, we will replace it for a *binary classifier*, the softmax aimed to predict "the probability of some class in comparison with all the others", while this binary classifier aims to predict "the probability of two things are connected"

So you will replace you data from:

| source | target |
| ------ | ------ |
| s1     | t1     |
| s1     | t2     |
| s2     | t3     |

to something like (using k=2)

| context | target | binary_target |
| ------- | ------ | ------------- |
| s1      | t1     | 1             |
| s1      | t98    | 0             |
| s1      | t33    | 0             |
| s1      | t2     | 1             |
| s1      | t99    | 0             |
| s1      | t31    | 0             |
| s2      | t1     | 1             |
| s2      | t99    | 0             |
| s2      | t37    | 0             |

and now we train the model, which is now a model that maps 
$$\displaystyle \Huge \begin{eqnarray} 
context, target \rightarrow binary\_target
\end{eqnarray}$$

So instead of modelling:
$$\displaystyle \Huge \begin{eqnarray} 
p(t \mid c) = softmax(e_t^T\cdot e_c)
\end{eqnarray}$$
we will model (using [[Sigmoid function|sigmoid]]):
$$\displaystyle \Huge \begin{eqnarray} 
p(y=1\mid c,t) = \sigma(e_t^T\cdot e_c)
\end{eqnarray}$$

---

The problem is *how to choose the negative sampling* (t98, t33, t99, t31, ....), that might or might not be equal to all the positive samples.

Another point is, it is OKAY if by chance I ended up choosing a negative sampling that is a positive sampling - like (s1, t1) on the example

>[!note]
>There is this heuristic of using k between 5 to 20 if the dataset is small, and 2 to 5 if the dataset is big

