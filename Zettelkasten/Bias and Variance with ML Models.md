---
tags:
  - machine-learning
---
[[Machine Learning]] models have two concepts deeply connected with [[underfitting]] and [[overfitting]].

We can say that a model has *low/high* **bias** and *low/high* **variance**.

**Bias:**
-  **High bias:** The model makes *incorrect predictions* even on the training data because it relies on *overly simplistic assumptions*, leading to systematic errors - [[underfitting]]
-  **Low bias:** The model makes *accurate predictions on the training data* because it has successfully *learned the patterns it was trained on*.

**Variance:**
- **High variance:** The model is *too sensitive to small fluctuations in the training data*, meaning it *memorises specific examples rather than capturing general patterns*. This leads to **poor generalisation to unseen data** - [[overfitting]].
- **Low variance:** The model remains **stable across different training samples**, meaning *different training datasets will produce similar models*. This helps with generalisation ability, improving performance on unseen data.

*We are looking for a model that is **low bias and low variance***. [[Trade-off between bias and variance]].