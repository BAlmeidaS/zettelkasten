---
tags:
  - Calculus
---
In 3-dimensions, *curl* is used to describe the rotation or rotational tendency of a field, often applied to fluid flows in three dimensions. 

The curl of a vector field measures the amount of "twist" or circular motion at a point in the field. For a fluid, this would correspond to how much and in what way the fluid is rotating around a point.

*curl* is defined as the [[Cross product]] of the [[vector field]] $\displaystyle \large \vec{V}$ and [[Vector nabla|nabla]]([[partial derivatives]]):
$$\displaystyle \Huge \begin{eqnarray} 
curl\ \vec{V} &=& \nabla \times \vec{V} \\
curl\ \vec{V} &=& 
\left(
\dfrac{\partial v_3}{\partial y} - \dfrac{\partial v_2}{\partial z} 
\right)\hat{i} +
\left(
\dfrac{\partial v_1}{\partial z} - \dfrac{\partial v_3}{\partial x} 
\right)\hat{j} +
\left(
\dfrac{\partial v_2}{\partial y} - \dfrac{\partial v_1}{\partial z} 
\right)\hat{i}
\end{eqnarray}$$

being $\displaystyle \large v_1$ the component on the $\displaystyle \large x$ dimension $\displaystyle \large \hat{i}$
being $\displaystyle \large v_2$ the component on the $\displaystyle \large y$ dimension $\displaystyle \large \hat{j}$
being $\displaystyle \large v_3$ the component on the $\displaystyle \large z$ dimension $\displaystyle \large \hat{k}$

![[Pasted image 20240129164248.png|500]]

*curl and cross-product start with C*

---

$$\displaystyle \Huge \begin{eqnarray} 
det \left(\begin{bmatrix}
\hat{i} & \hat{j} & \hat{k} \\ 
dx & dy & dz \\ 
x & y & z \\ 
\end{bmatrix}
\right) = cross\ product
\end{eqnarray}$$