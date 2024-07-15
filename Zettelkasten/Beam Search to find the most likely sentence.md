---
tags:
  - machine-learning
---
When on a [[Sequence to Sequence models]] one way to find the *best sentence to be generated*:
$$\displaystyle \Huge \begin{eqnarray} 
\arg \max_y p(y^{<1>}, \cdots, y^{<T_y>} \mid \boldsymbol{x})
\end{eqnarray}$$
It is using [[Beam Search]], and here an example to show how can be used.

##### Step 1
Assume a vocabulary of 10,000 thousand words:
![[Pasted image 20240714194734.png|150]]
The first $\displaystyle \large y^{<1>}$ will be one based on the distribution of $\displaystyle \large p(y^{<1>} \mid x)$:
![[Pasted image 20240714194946.png|300]]
Based on a *hyperparameter* $\displaystyle \large B$ (let's say 3 for this example) we will get from the [[softmax function|softmax]] resultant as $\displaystyle \large y^{<1>}$ of the $\displaystyle \large B$ *most likely words and keep on memory*. 

##### Step 2
*Each of the $\displaystyle \large B$ words selected will be used as input to generate the next y*, $\displaystyle \large y^{<2>}$. Thus, $\displaystyle \large B$ new outcomes *will be evaluated for each one of the initial ones*:
$$\displaystyle \Huge \begin{eqnarray} 
p(y^{<2>} \mid \boldsymbol{x}, y^{<1>})
\end{eqnarray}$$
![[Pasted image 20240714200851.png|500]]

At the end what we want is to find the *sequence generated* that is most likely:
$$\displaystyle \Huge \begin{eqnarray} 
\arg \max_y p(y^{<1>}, y^{<2>} \mid \boldsymbol{x}) = 
\arg \max_y p(y^{<1>} \mid \boldsymbol{x}) *
p(y^{<2>} \mid \boldsymbol{x}, y^{<1>})
\end{eqnarray}$$

At the end of the step 2, *there will be $\displaystyle \large B*vocab$ results evaluated*, and based on the *sequence generated until that point*, we will get *the $\displaystyle \large B$ most likely*.

##### Step n
The algorithm keeps until all $\displaystyle \large B$ sequences include the end-of-sequence and we get the one with highest probability.

##### Others
The fact that multiplying many numbers that are way smaller than 1 results in a tiny number might lead to a problem of [[underflow]]. Thus, one solution is maximising the [[likelihood|log likelihood]] instead:
$$\displaystyle \Huge \begin{eqnarray} 
&&\arg \max_y p(y^{<1>}, \cdots, y^{<T_y>} \mid \boldsymbol{x}) = 
\\[5pt]
&=& \arg \max_y \prod^{T_y}_{t=1} p(y^{<t>} \mid \boldsymbol{x}, y^{<1>}, \dots, y^{<t-1>})
\\[5pt]
&=& \arg \max_y \sum^{T_y}_{t=1} \log p(y^{<t>} \mid \boldsymbol{x}, y^{<1>}, \dots, y^{<t-1>}) \\
\end{eqnarray}$$

*Another problem* is that the *objective function, as defined so far, tends to prefer* **short sentences**, even with the log likelihood. Thus **normalising by the size of the sentence** removes this effect:
$$\displaystyle \Huge \begin{eqnarray} 
\arg \max_y \dfrac{1}{{T_y}^\alpha} \sum^{T_y}_{t=1} \log p(y^{<t>} \mid \boldsymbol{x}, y^{<1>}, \dots, y^{<t-1>}) \\
\end{eqnarray}$$
With $\displaystyle \large \alpha$ varying from $\displaystyle \large 0$ (not normalised) to $\displaystyle \large 1$ (completely normalised).
