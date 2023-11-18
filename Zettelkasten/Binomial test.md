---
tags:
  - Statistics
aliases:
  - binomial test
  - prop test
---
A test that can be used to determine whether the *observed proportion of success in a **binary outcome** experiment differs from a hypothesised proportion*.

[[Null Hypothesis|H0]]: The population proportion is equal to the specific hypothesised value
[[Alternative Hypothesis|H1]]: The population proportion is different to the specific hypothesised value

the [[Hypothesis Test|Statistical Test]] is the *probability calculation* of getting that value that we are observing with that chance informed.

For Instance:

- If we have 3 success among 16 data points observed. Can this distribution being explained by a binomial of $\displaystyle \large p=0.5$:
![[Pasted image 20231107193513.png]]
Answer: *$\displaystyle \large \text{p-value} \lt 0.05$, we reject $\displaystyle \large H0$, so 3:16 is not a binomial with proportion of $\displaystyle \large 50\%$.*

---

In `R` we can use `prop.test` to compare two proportions
- Let's say that we have two proportions, 4 out of 40 and 196 out of 3270, we can run:
![[Pasted image 20231107195417.png]]