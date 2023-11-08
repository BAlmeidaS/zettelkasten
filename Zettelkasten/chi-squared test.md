---
tags:
  - Statistics
---
A test to validate if there is a *association between two categorical variables*.

[[Null Hypothesis|H0]]:  *They are independent* / There is no significant association between the categorical variables
[[Alternative Hypothesis|H1]]:  *They are dependent on each other* / There is a significant association between the categorical variables

Since you have two [[Categorical variable|categorical variables]], you have a [[Contingency Table]], something like this:

|           | Blue eyes | Brown eyes |
| --------- | --------- | ---------- |
| Fair Hair | 38        | 11         |
| Dark Hair | 14        | 51         |

You will complete the table with *total rows*, *total cols* and *total measurements*

|               | Blue eyes | Brown eyes | Row totals |
| ------------- | --------- | ---------- | ---------- |
| Fair Hair     | 38        | 11         | 49         |
| Dark Hair     | 14        | 51         | 65         |
| Column totals | 52        | 62         | 114        |

If they are *independent* the chance of an observation *is the chance of one category TIMES the other category* - for instance, the chance to be Blue eyes and Fair Hair should be $\displaystyle \large \dfrac{49}{114} * \dfrac{52}{114} * 114 = 22.35$, and this we call *expected frequency*.

So, the *expected frequency of a cell** is:

