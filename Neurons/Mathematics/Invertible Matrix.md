#LinearAlgebra 

The invertible matrix of a $2 \times 2$ square matrix is found by

1. Finding the [[Determinant]] of the matrix
2. Finding the [[Adjugate]] of the matrix
3. Dividing as $\frac{adj}{det}$

The invertible matrix of a $3 \times 3$ matrix is found by taking the augmented matrix, $[A | I]$, and computing the gaussian elimination transformations to get $I$ from $A$. For independent matrices, this will work as an $n \times n$ matrix $I$ represents the fundamental basis vectors for any independent $n \times n$ matrix $A$.

A matrix $A$ is considered to be invertible when $AA^{-1} = A^{-1}A = I$

If the [[determinant]] of a given matrix is $0$, it is not invertible and therefore is linearly dependent as the $0 \hspace{1.5mm} det()$ implies that it adds no information as it doesn't transform the given $\mathbb{R}^n$ space.

Note that the invertible matrix $A^{-1}$, when matrix multiplied onto $A$, it will produce $I$. The order, whether $AA^{-1}$ or $A^{-1}A$ does not matter. Both will produce the identity matrix, $I$.

Using the invertible matrix, you can solve a [[Systems of Linear Equations]] as $x = A^{-1}b$.


