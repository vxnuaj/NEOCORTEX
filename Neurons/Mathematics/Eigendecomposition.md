#LinearAlgebra 

Eigendecomposition expresses a square matrix $A$ in terms of it's eigenvalues and eigenvectors. 

> $A$ does not have to be full-rank.

$A = V\Lambda V^-1$

where 

- $V$ is a matrix whose columns are eigenvectors of $A$
- $\Lambda$ is a diagonal matrix, containing the eigenvalues of all $A$ on the diagonal

Given $A$, we have an [[eigenvalue]] and an [[eigenvector]] that satisfies:

$Av = \lambda v$

When we apply a linear combination of the column vectors of $A$ with $v$ as $Av$, we get a multiple of $v$, the multiplier denoted by $\lambda$ which is the [[eigenvalue]] and the [[eigenvector]] is $v$.

To solve for eigenvectors and eigenvalues:

1. Find the characteristic polynomial, via $det(A - \lambda I)$
2. Solve for each $\lambda$ in the characteristic polynomial
3. Solve for each eigenvector, $v$, by plugging $\lambda$ into $A - \lambda I$

and to finally perform eigendecomposition, $A = V\Lambda V^-1$:

1. Plug in each eigenvalue into the diagonal matrix, $\Lambda$.
2. Plug in the corresponding eigenvector to each column vector in $\Lambda$, they must be same indices. Index of eigenvalue column in $\Lambda$ must be the same as index of eigenvector in $V$.


---


why do we solve for zero vector when finding eigenvectors?