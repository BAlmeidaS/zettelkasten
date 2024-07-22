---
tags:
  - deep-learning
aliases:
  - face recognition
  - face verification
---
A Siamese Network is a type of [[Neural networks]] that consists of two or more identical sub-networks sharing the same parameters and weights.

These sub-networks process two different input vectors to produce output vectors.

The primary purpose of Siamese Networks is to determine the similarity between the input vectors by comparing their outputs. Useful to solve [[One Shot Learning]], they achieved good results on *DeepFace* to build *face recognition*
![[Pasted image 20240722141117.png]]

The Idea is measuring the [[Similarity function|similarity]] between $\displaystyle \large y_1$ and $\displaystyle \large y_2$ in order to say if this two people are the same, by getting the output vector of this [[Convolutional Neural Network|CNN]] and considered as an [[embedding]].

Two ways to tackle this problem:
1. Using [[Triplet Loss]] as loss function (*face recognition - 1:k problem*)
2. concatenate at the end a logistic regression and treat this problem as a *binary classification problem* (*face verification - 1:1 problem*)
![[Pasted image 20240722163438.png]]

For the 2. case, using [[Sigmoid function]]:
$$\displaystyle \Huge \begin{eqnarray} 
\hat{y} = \sigma\left(\sum\limits^{n_b}_{k=1} w_k\vert f(x_i)_k - f(x_j)_k \vert + b \right)
\end{eqnarray}$$

Or even using the [[chi-squared similarity]]:
$$\displaystyle \Huge \begin{eqnarray} 

\hat{y} = \sigma\left(\sum\limits^{n_b}_{k=1} w_k
\left(
\dfrac{(f(x_i)_k - f(x_j)_k)^2}
{(f(x_i)_k + f(x_j)_k)}
\right) + b \right)
\end{eqnarray}$$