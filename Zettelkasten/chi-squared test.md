---
tags:
  - Statistics
---
A test to validate if there is an *association between two categorical variables*.

[[Null Hypothesis|H0]]:  *The two category variables are independent* / There is no significant association between the categorical variables
[[Alternative Hypothesis|H1]]:  *The two category vars are dependent on each other* / There is a significant association between the categorical variables

*If two variables are independent, it means that knowledge of one does not provide useful information about the other. For instance, if you're looking at the relationship between eye colour and reading preference in a population and find them to be independent, knowing a person's eye colour doesn't help you predict their reading preference, and vice versa.*

Since you have two [[Categorical variable|categorical variables]], you have a [[Contingency Table]], with the **observed frequencies**:

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

So, the **expected frequency of a combination of categories** is:
$$\displaystyle \Huge \begin{eqnarray} 
E &=& \dfrac{R \times C}{G} \\ \\
R &\rightarrow& \text{Row Total} \\
C &\rightarrow& \text{Column Total} \\
G &\rightarrow& \text{Grand Total}
\end{eqnarray}$$

With this you will mount a table with the **expected frequencies**:

|               | Blue eyes | Brown eyes | Row totals |
| ------------- | --------- | ---------- | ---------- |
| Fair Hair     | 22.35     | 26.65      | 49         |
| Dark Hair     | 29.65     | 35.35      | 65         |
| Column totals | 52        | 62         | 114        |

The [[Test Statistic]] $\displaystyle \large \chi^2$ , is defined as:
$$\displaystyle \Huge \begin{eqnarray} 
\chi^2 &=& \sum\dfrac{(O-E)^2}{E} \\\\
O &\rightarrow& \text{Observed Category} \\
E &\rightarrow& \text{Expected Category}
\end{eqnarray}$$

**Finally**, $\displaystyle \large \chi^2$ must be compared with the quantile of the *chi-square (with n d.f.) distribution* related to the alpha level that you want.

1. [[Degrees of Freedom]] on [[Contingency Table]] are defined as:
$$\displaystyle \Huge d.f. = (r-1)*(c-1)$$
This happens because row total, column total and Grand total, impose a significant reduce in degrees of freedom. For instance, 2 x 2 table, we have $\displaystyle \large d.f.=1$.

2. Defined an [[Significance Level|alpha level]] like, $\displaystyle \large \alpha = 0.05$, you can search on a chi-square distribution:
> [!R Lang]
> `qchisq(0.95, 1)`

---

The whole test in `R` can be executed as:
> [!R Lang]
> ```R
> count <- matrix(c(38, 14, 11, 51), ncol=2)
> chisq.test(count)
> ``` 
> or even with table:
> ```R
> chisq.test(table(df$col1, df$col2))
> ```
