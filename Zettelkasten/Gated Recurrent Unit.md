---
tags:
  - deep-learning
aliases:
  - GRU
---
Created as an extension of default [[Recurrent Neural Network|RNNs]] to solve their [[vanishing gradient problem]]. Important to notice that *GRU* came after than [[Long Short-Term Memory|LSTM]], almost 17 years after, and it is "kind of" a simplification of [[Long Short-Term Memory|LSTM]].

The main idea is based on *gates* $\displaystyle \large \Gamma$, that controls how much of the context $\displaystyle \large a^{<t-1>}$ will pass, defined using a [[Sigmoid function]] $\displaystyle \large \sigma$ (that varies from 0 to 1 to be the gate):
$$\displaystyle \Huge \begin{eqnarray} 
\Gamma_i = \sigma(M_i*x^{<t>} + U_i*a^{<t-1>} + b_i) 
\end{eqnarray}$$
$\displaystyle \large M, U, b$ are [[Parameters of the Model|Parameters]] *of the gate*. 

>[!note]
>A "simplified version" using the [[Multiple weights simplification notation]]:
>$$\displaystyle \Huge \begin{eqnarray} 
>\Gamma_i = \sigma(W_i[x^{<t>}, a^{<t-1>}] + b_i) 
>\end{eqnarray}$$

*GRU gates* , *G*ates *R* and *U*:

| Symbol                          | Name of the gate | Role                               |
| ------------------------------- | ---------------- | ---------------------------------- |
| $\displaystyle \large \Gamma_r$ | Relevance gate   | *Drop previous information?*       |
| $\displaystyle \large \Gamma_u$ | Update gate      | *How much past should matter now?* |

Instead of using activation as $\displaystyle \large a^{<t>}$, GRU define what is called *memory cell* $\displaystyle \large c^{<t>}$, that in this context is exactly the same as $\displaystyle \large a^{<t>}$, so here, $\displaystyle \large a^{<t>} = c^{<t>}$.


There are *two memory cells*, the candidate $\displaystyle \large \tilde{c}^{<t>}$ and the final memory cell $\displaystyle \large c^{<t>}$. Here we are using the [[Multiple weights simplification notation]] and [[element-wise multiplication|element-wise product]]:
$$\displaystyle \Huge \begin{eqnarray} 
\tilde{c}^{<t>} &=& tanh(W_c[\Gamma_r \odot a^{<t-1>},x^{<t>}] + b_c)
\\[6pt]
c^{<t>} &=& \Gamma_u \odot \tilde{c}^{<t>} + (1 - \Gamma_u) \odot c^{<t-1>}
\end{eqnarray}$$

![[Pasted image 20240708171640.png|400]]

>[!hint]
>$\displaystyle \large c^{<t>}$ (and in consequence $\displaystyle \large a^{<t>}$) is a vector, with each "bit" meaning one context, the gate $\displaystyle \large \Gamma$ is [[element-wise multiplication|element-wise multiplied]] to $\displaystyle \large c$ in order to control on the point that the sentence is only some bits of this context. Thus, allowing the context to be as complex as the size of $\displaystyle \large c$.
