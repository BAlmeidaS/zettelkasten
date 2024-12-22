---
tags:
  - machine-learning
---
A way to evaluate [[Clustering]] using [[Hypothesis Test]]

1. **Generate Randomised Labels:**
    - Randomly shuffle the labels assigned to your data points while keeping the cluster sizes constant. This creates a randomised partition of the data.
2. **Compute Test Statistic:**
    - Calculate a test statistic (e.g., cluster silhouette score, within-cluster sum of squares, or any other relevant metric) for both the actual clustering and the randomised labelling.
3. **Repeat Randomisation:**
    - Repeat steps 1 and 2 a sufficient number of times to create a distribution of the test statistic under the null hypothesis (random labelling).
4. **Compare Observed Test Statistic:**
    - Compare the observed test statistic from your actual clustering to the distribution of test statistics obtained from the randomisation.
5. **Calculate P-value:**
    - Determine the proportion of randomised labelling that result in a test statistic as extreme as or more extreme than the observed test statistic. This proportion represents your p-value.
6. **Interpret Results:**
    - If the p-value is small (typically below a predefined significance level like 0.05), you reject the null hypothesis and conclude that your clustering result is significantly different from random chance.
    - If the p-value is not small, you fail to reject the null hypothesis, indicating that your clustering result is not significantly different from random chance.