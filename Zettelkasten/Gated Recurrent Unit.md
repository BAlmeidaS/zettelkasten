---
tags:
  - deep-learning
aliases:
  - GRU
---
Created as an extension of default [[Recurrent Neural Network|RNNs]] to solve their [[vanishing gradient problem]].


The main idea is creating a *gate* $\displaystyle \large \Gamma$, that controls how much of the context $\displaystyle \large a^{<t-1>}$ will pass, defined using a [[Sigmoid function]] $\displaystyle \large \sigma$ (that varies from 0 to 1 to be the gate):
$$\displaystyle \Huge \begin{eqnarray} 
\Gamma = \sigma(W*x^{<t>} + U*a^{<t-1>} + b)
\end{eqnarray}$$
$\displaystyle \large W, U, b$ are [[Parameters of the Model|Parameters]] *of the gate*.

 
*GRU gates* defines two gates:

| Symbol                          | Name of the gate | Role                               |
| ------------------------------- | ---------------- | ---------------------------------- |
| $\displaystyle \large \Gamma_u$ | Update gate      | *How much past should matter now?* |
| $\displaystyle \large \Gamma_r$ | Relevance gate   | *Drop previous information?*       |





*GRU* extends *RNN* by adding a *memory cell* $\displaystyle \large c$, and in the context of GRU, $\displaystyle \large c^{<t>}$ may be interpreted as $\displaystyle \large a^{<t>}$.

