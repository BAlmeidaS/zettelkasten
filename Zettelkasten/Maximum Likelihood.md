---
tags:
  - Statistics
---
[[Statistics]] method used to choose the *best* [[Parameters of the Model|parameters]] of a model by selecting the values that has the *maximum likelihood* with the given observing data.

1. given the data
2. given our choice of model
3. what values of the [[Parameters of the Model]] make the observed data most likely?


Mathematically speaking, we want to find the parameters $\displaystyle \large \Theta$ of the model, that maximise the [[likelihood]] of all that points occur. Being $\displaystyle \large L$ the likelihood and $\displaystyle \large n$ the number of datapoints, we can calculate the [[likelihood|log likelihood]] as:
$$\displaystyle \Huge \begin{eqnarray} 
\log L(\Theta) &=& \sum^n_{i=1} \log P(x_i \mid \Theta)
\end{eqnarray}$$


The *ideal set of parameters $\displaystyle \large \Theta$ is the one that maximise the **log-likelihood**.* This set of parameters is called *maximise the log-likelihood function*:
$$\displaystyle \Huge \begin{eqnarray} 
\Theta_{MLE}
&=& \arg\max_{\Theta} \log L(\Theta) \\
&=& \arg\max_{\Theta} \sum^n_{i=1} \log P(x_i \mid \Theta)\\
\end{eqnarray}$$

---

In the case of binary classifiers, the probability $\displaystyle \large P(x_i\mid\Theta)$ can be defined using [[Bernoulli distribution]].

