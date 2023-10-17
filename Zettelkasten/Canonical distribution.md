In [[Bayesian Network|Bayes Net]] can be quite painful to define every entry on the [[Conditional probability table|CPT]]s. For many time, instead of defining the whole table, we end up defining a *pattern* which reduces the amount of information that we have to fill in on the table.

This is a way to parameterise and represent probability distributions over sets of variables in a *more compact* way. The idea is using distributions as [[Gaussian]], [[Poisson]], [[Bernoulli]], ...

---
*Let's say you have a node in a Bayesian network with multiple parents, and each parent can take on several values. Defining a full CPT for that node would require specifying a probability for every possible combination of parent values, which can become impractical for large networks. By using a canonical distribution, you can capture the relationships and dependencies among the variables in a more compact way.*