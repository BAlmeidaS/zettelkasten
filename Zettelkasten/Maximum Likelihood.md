---
tags:
  - Statistics
cssclasses:
  - wider_page.css
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


>[!example]
>Let's consider a simple dataset to create a *binary classifier*, it will have one continuous [[Explanatory variable|independent variable]] and the binary [[Response variable|dependent variable]]. This is the plot of the data:
>![[Pasted image 20250204003551.png|200]]
>
>Then we fit some [[logistic regression]]:
>![[Pasted image 20250204003706.png|200]]
>
>The goal is to find the model with **the maximum likelihood**. To do this, we will get the [[Log Odds]] of the probability, going from the plot above, to this one below:
>![[Pasted image 20250204003915.png|200]]
>
>Then we project each point to the candidate line (the logistic regression itself, but here represented using log odds):
>![[Pasted image 20250204004013.png|200]]
>
>Then, by using the [[Log Odds|inverse log odds]], we transform back the projections to probability:
>![[Pasted image 20250204004129.png|200]]
>
>The **likelihood of this model will be *the PRODUCT of the blue points being blue* $\displaystyle \large \times$ *the product of the red points being red***, for instance:
>$$\displaystyle \Huge \begin{eqnarray} 
>L(\Theta) &=& 
>\overbrace{0.49*0.8*0.91*0.91*0.92}^{\text{probability of the 5 blue points being blue}}
>*
>\underbrace{(1-.01) * (1-0.01)*(1-0.3)*(1-0.9)}_{\text{probability of the 4 red points being red}}
>\end{eqnarray}$$
>
>but instead of calculating the product, we apply [[likelihood|log likelihood]] simply because its easier.
>
>$$\displaystyle \Huge \begin{eqnarray} 
>
>\log L(\Theta) &=& 
>0.49*0.8*0.91*0.91*0.92
>\\ &&*
>(1-.01) * (1-0.01)*(1-0.3)*(1-0.9)
>\\ &=&
>\log(
>0.49*0.8*0.91*0.91*0.92
>\\&&\ \ \ \ \ \ \ *
>(1-.01) * (1-0.01)*(1-0.3)*(1-0.9)
>)
>\\ &=&
>\log 0.49  + \log 0.8 + \log 0.91 + \log 0.91 + \log 0.92
>\\ &&+
>\log (1-.01) + \log (1-0.01) + \log (1-0.3) + \log (1-0.9)
>\end{eqnarray}$$
>
>which in the example is:
>$$\displaystyle \Huge \begin{eqnarray} 
>\log L(\Theta) = -3.77
>\end{eqnarray}$$
> *The goal here is *rotating the line on the log odds and finding the **maximumm log-likelihood**

---

In the case of binary classifiers, the probability $\displaystyle \large P(x_i\mid\Theta)$ can be defined using [[Bernoulli distribution]].

