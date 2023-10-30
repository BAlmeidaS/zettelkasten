---
tags:
  - Russel-n-Norvig-chap-23
---
The idea is, whenever we have an [[N-gram word model]] that for some n-gram on the text has zero probability (or really low) we back off the model to *(n-1).gram*. The idea is reducing the [[Variance of the model]] 

---
There is an strategy that a backoff model could be a [[linear combination]] of the 3 models, trigram, bigram and unigram models.
$$\displaystyle \Huge \begin{eqnarray} 
\hat P(c_i\mid c_{i-2:i-1}) &=& \lambda_3P(c_i\mid c_{i-2:i-1}) + \lambda_2P(c_i\mid c_{i-1}) + \lambda_1P(c_i) \\ \\
& &\ \lambda_1 + \lambda_2+\lambda_3 = 1
\end{eqnarray}$$