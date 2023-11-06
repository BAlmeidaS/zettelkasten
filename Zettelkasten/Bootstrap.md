---
tags:
  - Statistics
---
A completely different way to calculate [[Confidence Interval]]. Bootstrap is by definition a [[Non-parametric Method]]

*You have a single sample of n measurements, that you will collect many times sample from it. **The samples got MUST BE WITH REPLACEMENT**, then you Calculate the mean of each sample that you get*. You obtain the [[Confidence Interval]] by looking at the extreme highs and lows values of the estimated means (getting from the [[Percentile]] that you want).

For instance, if you want to get 95% of CI, you want to get the 2.5 percentile and 97.5 percentile of the distribution of the sample means.

**The estimates of CI from the bootstrap and the normal theory are not the same**. Though they are very close.