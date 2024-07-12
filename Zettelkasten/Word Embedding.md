---
tags:
  - deep-learning
---
An [[embedding]] for words. A good think about word embedding is that the dimensions of the embedding might be related to the "meaning" of the word. Rather then [[One-Hot Enconding]], they tend to use better the space ([[dense vector]]) and thus have [[Similarity function|similarity]] embedded. 

![[Pasted image 20240710144712.png|500]]

The simplest *embedding* is what some researches called [[Shallow encoder embedding|Shallow embedding]] and the goal would be learning the matrix $\displaystyle \large E$.

The interesting thing is that you can make vector operations to understand what is the meaning, like the example of *man is to king as woman is to ?* (queen) By using [[Arg Max]] we can solve it as:
$$\displaystyle \Huge \begin{eqnarray} 
e_{man} - e_{woman} &\approx& e_{king} - e_{w}
\\[10pt]
w &:=& \arg\max_w similarity(e_w, e_{king} - (e_{man} - e_{woman}))
\end{eqnarray}$$

The most common [[Similarity function|similarity]] used in *word embedding* is [[cosine similarity]]

---

The easiest way to learn *word embedding* is by using context, so given a phrase with $\displaystyle \large n$ words, you can use the last $\displaystyle \large k$ words to predict the next word. To do so, one approach will be building a [[Neural networks]] that receives these $\displaystyle \large k$ words and predicts the next. 

The goal will be defining the matrix $\displaystyle \large E$ ([[Shallow encoder embedding|shallow embedding]]) and fitting on a network that:
1. transform the k words from [[One-Hot Enconding]] (vocabulary size, $\displaystyle \large v$) to the embedding using this $\displaystyle \large E$
2. stacking fully connected layers to predict at the end $\displaystyle \large v$ numbers (vocabulary size)
3. apply [[softmax function|softmax]] to attach a probability to the words and than sample from it.

This works well but there are other algorithms that do better jobs, such as:
- [[Skip-gram Model]]
- [[Word2Vec]]
- [[Global Vectors for Word Representation]]


---

They are learned *automatically* by the data. Unlikely pre-trained models, *word embeddings produced for a specific task tend to emphasise aspects of words that are useful for that task*. [[Example of a word embedding being created to solve a POS problem]]

![[Pasted image 20231101192053.png|600]]