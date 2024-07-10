---
tags:
  - deep-learning
---
An [[embedding]] for words. A good think about word embedding is that the dimensions of the embedding might be related to the "meaning" of the word. Rather then [[One-Hot Enconding]], they tend to use better the space and thus have [[Similarity function|similarity]] embedded

![[Pasted image 20240710144712.png|500]]

The simplest *embedding* is what some researches called [[Shallow encoder embedding|Shallow embedding]].

The interesting thing is that you can make vector operations to understand what is the meaning, like the example of *man is to king as woman is to ?* (queen) By using [[Arg Max]] we can solve it as:
$$\displaystyle \Huge \begin{eqnarray} 
e_{man} - e_{woman} &\approx& e_{king} - e_{w}
\\[10pt]
w &:=& \arg\max_w similarity(e_w, e_{king} - (e_{man} - e_{woman}))
\end{eqnarray}$$

The most common [[Similarity function|similarity]] used in *word embedding* is [[cosine similarity]]