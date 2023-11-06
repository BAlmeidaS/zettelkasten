---
tags:
  - Statistics
---
*Student's t distribution*, the one used to calculate [[Values of Student's T]] are *preferable* instead of [[Normal Distribution]] *when the sample sizes are small ($\displaystyle \large n<30$)*. 

*Extreme values are more likely with a t distribution than with a normal.*

After $\displaystyle \large n>30$, student's T behaves almost as a normal

in `R` the equivalent of `rnorm` and `pnorm` are `qt` and `pt`.

Student's T produce "wider" functions then normals.
![[Pasted image 20231106183944.png|700]]