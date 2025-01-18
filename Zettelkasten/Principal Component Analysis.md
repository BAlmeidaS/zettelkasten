---
tags:
  - machine-learning
  - Statistics
aliases:
  - PCA
---
A full comprehensive derivation of *PCA* can be found in [[Principal Component Analysis - Derivation]]. 

PCA assumes that the *data is centred* ([[Average|Mean]] = 0). Thus, [[mean-normalisation]] is recommended.

PCA relies on calculating the [[Covariance Matrix]] and having the data normalised *helps to reduce numerical instabilities with large numbers*.


>[!note] summary
> A summary about *PCA* is, from the [[Covariance Matrix]] of a dataset, you calculate the [[eigenvalue|eigenvalues]], and from them, the [[eigenvector|eigenvectors]].
>
> The [[eigenvector|eigenvectors]] are the *principal components* and you rank them by their [[eigenvalue|eigenvalues]].
>
> The [[eigenvalue|eigenvalues]] are the variance that the *principal component* explains, which means the higher the better. We want to keep the [[eigenvector|eigenvectors]] related to the highest [[eigenvalue|eigenvalues]] and remove the ones related to the low, since they bring low information


Each data point $\displaystyle \large x$ will be [[The orthogonal projection into ND subspaces|projected]] to the new [[orthonormal basis]] made by the first [[eigenvector|eigenvectors]]. The matrix with the [[eigenvector|eigenvectors]] used, as columns, is called $\displaystyle \large B$.

The projection will be called $\displaystyle \large \tilde{x}$:
$$\displaystyle \Huge \begin{eqnarray} 
\tilde{x} = \pi_u (x) = BB^Tx

\end{eqnarray}$$

Being $\displaystyle \large B^Tx$ the *coordinates* of the projection of $\displaystyle \large x$ with respect to [[orthonormal basis]] created with the *firsts* [[eigenvector|eigenvectors]]/*principal components*.

