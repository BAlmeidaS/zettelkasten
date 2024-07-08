---
tags:
  - deep-learning
aliases:
  - LSTM
---
Created as an extension of default [[Recurrent Neural Network|RNNs]] to solve their [[vanishing gradient problem]]. More powerful than [[Gated Recurrent Unit|GRU]].

As in *GRU*, the main idea is based on *gates* $\displaystyle \large \Gamma$, that controls how much of the context $\displaystyle \large a^{<t-1>}$ will pass, defined using a [[Sigmoid function]] $\displaystyle \large \sigma$ (that varies from 0 to 1 to be the gate):
$$\displaystyle \Huge \begin{eqnarray} 
\Gamma_i = \sigma(M_i*x^{<t>} + U_i*a^{<t-1>} + b_i) 
\end{eqnarray}$$
$\displaystyle \large M, U, b$ are [[Parameters of the Model|Parameters]] *of the gate*. 

>[!note]
>A "simplified version" using the [[Multiple weights simplification notation]]:
>$$\displaystyle \Huge \begin{eqnarray} 
>\Gamma_i = \sigma(W_i[x^{<t>}, a^{<t-1>}] + b_i) 
>\end{eqnarray}$$

*LSTM Gates*:

| Symbol                          | Name of the gate | Role                               |
| ------------------------------- | ---------------- | ---------------------------------- |
| $\displaystyle \large \Gamma_r$ | Relevance gate   | *Drop previous information?*       |
| $\displaystyle \large \Gamma_u$ | Update gate      | *How much past should matter now?* |
| $\displaystyle \large \Gamma_f$ | Forget gate      | *Erase a cell or not?*             |
| $\displaystyle \large \Gamma_o$ | Output gate      | *How much to reveal of a cell?*    |

On *LSTM* the activation $\displaystyle \large a^{<t>}$ is not equal to $\displaystyle \large c^{<t>}$, rather is controlled by the output gate. Also there is a Forget gate (replacing the $\displaystyle \large 1-\Gamma_u$ from [[Gated Recurrent Unit|GRU]]).

The are *two memory cells*, the candidate $\displaystyle \large \tilde{c}^{<t>}$ and the final memory cell $\displaystyle \large c^{<t>}$ are defined as (using the [[Multiple weights simplification notation]] and [[element-wise multiplication|element-wise product]]):
$$\displaystyle \Huge \begin{eqnarray} 
\tilde{c}^{<t>} &=& tanh(W_c[\Gamma_r \odot a^{<t-1>},x^{<t>}] + b_c)
\\[6pt]
c^{<t>} &=& \Gamma_u \odot \tilde{c}^{<t>} + \Gamma_f \odot c^{<t-1>}
\\[6pt]
a^{<t>} &=& \Gamma_o \odot tanh(c^{<t>})
\end{eqnarray}$$

![[Pasted image 20240708182107.png|400]]

>[!hint]
>$\displaystyle \large c^{<t>}$ (and in consequence $\displaystyle \large a^{<t>}$) is a vector, with each "bit" meaning one context, the gate $\displaystyle \large \Gamma$ is [[element-wise multiplication|element-wise multiplied]] to $\displaystyle \large c$ in order to control on the point that the sentence is only some bits of this context. Thus, allowing the context to be as complex as the size of $\displaystyle \large c$.