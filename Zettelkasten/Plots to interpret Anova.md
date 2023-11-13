---
tags:
  - Statistics
---
There are 2 traditional ways of plotting results of [[Analyse of Variance|Anova]]:
- [[Boxplot]]
- Bar plots

*Boxplots* should be drawn with `(notch=True)`

*Barplots* must add an error bar. This can be created using the [[Student's t = 2 rule of thumb]], of getting 2 [[Standard Error of the mean]]. You can also calculate *LSD bars* using [[Standard error of the difference between two mean]] and the thumb rule of 2 SE:
```R
lsd <- qt(0.975, d.f._diff_of_the_means) x SE_DIFF
```

*df_diff_of_the_means* is usually $\displaystyle \large N_A - 1 + N_B - 1$
