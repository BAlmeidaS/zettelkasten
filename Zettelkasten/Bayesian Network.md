Shows the dependencies among [[Random Variable]]s

A [[DAG - Directed Acyclic Graph]] such that:
1. Each node is a [[Random Variable]]
2. A link from X to Y shows that X is *parent* of Y
3. Each node $\displaystyle \large X_i$ has a probability info $\displaystyle \large \theta(X_i\mid Parents(X_i))$ - *Parents have a direct influence on Children*

For instance,
![[Pasted image 20231016014023.png|600]]

---
Also called, *Bayes Net*