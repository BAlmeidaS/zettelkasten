---
tags:
  - machine-learning
aliases:
  - softmax
---
*Softmax* transforms a *vector of real numbes into a vector of probabilities*. 

$$\displaystyle \Huge \begin{eqnarray} 
softmax(z_i) = \dfrac{e^{z_i}}{\sum^n_je^{z_j}}
\end{eqnarray}$$

The key properties:
1. **Probability Distribution**: The output values are in the range (0, 1) and sum to 1, making the vector interpretable as [[Probability Distributions|probability distribution]].
2. **Exponentiation and Normalisation**: The function uses exponentiation to ensure all values are positive, and normalisation by the sum ensures they sum to 1.
3. **Differentiability**: The softmax function is [[differentiable]], making it suitable for gradient-based optimisation methods used in training machine learning models.


![[Pasted image 20240614182154.png|400]]