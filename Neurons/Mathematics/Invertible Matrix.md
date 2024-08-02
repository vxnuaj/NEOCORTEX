#LinearAlgebra 

The invertible matrix of a square matrix is found by

1. Finding the [[Determinant]] of the matrix
2. Finding the [[Adjugate]] of the matrix
3. Dividing as $\frac{adj}{det}$


A matrix $A$ is considered to be invertible when $AA^{-1} = A^{-1}A = I$

If the [[determinant]] of a given matrix is $0$, it is not invertible and therefore is linearly dependent as the $0 \hspace{1.5mm} det()$ implies that it adds no information as it doesn't transform the given $\mathbb{R}^n$ space.

Using the invertible matrix, you can solve a [[Systems of Linear Equations]] as $x = A^{-1}b$.