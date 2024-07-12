---
tags:
  - deep-learning
---
A simple *deep learning model* to build [[Word Embedding]]. The idea is to create a dataset using [[Skip-gram]] and learn the [[Shallow encoder embedding|shallow embedding]] $\displaystyle \large E$.

*Continuous Bag of Word aims to predict the target from a context word*.

Usually the algorithm goes as the following:
1. The context is processed with [[One-Hot Enconding]], having the $\displaystyle \large o_{word}$
2. Then is multiplied by $\displaystyle \large E$ and having the [[embedding]] representation $\displaystyle \large e_{word}$
3. A dense layer is trained using the [[softmax function|softmax]] as non-linear function
4. the result is compared to $\displaystyle \large y$ from the [[Skip-gram]] (which is the target word)

The [[softmax function|softmax]] used on step 3 might be cost, because the result must be normalised by the size of the vocabulary (that might be 10,000, 100,000 or even bigger):
$$\displaystyle \Huge \begin{eqnarray} 
p(target\mid context) = \dfrac{
e^{\theta^T_{target}\cdot e_{context}}}{
\sum\limits^{vocab}_{i=0} 
e^{\theta^T_{i}\cdot e_{context}}}{
}
\end{eqnarray}$$

Being $\displaystyle \large \theta_{target}$ the parameters associated with the output $\displaystyle \large target$. 

A solution to avoid this linear computation might be [[Hierarchical Softmax]] another is [[negative sampling]]