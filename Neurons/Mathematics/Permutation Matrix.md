A permutation matrix is a binary matrix that holds exactly a single $1$ in each column or row while the rest of the components of the given column or row are $0$.

$P = \begin{bmatrix} 0, 0, 1 \\ 0, 1, 0 \\ 1, 0, 0 \end{bmatrix}$

They serve as a means to reorder the rows or columns of a matrix, when multiplied by it. 

If we have a permutation matrix $P_1$, and we want to swap a set of identified rows of $A$ a permutation of $A$ by $P_1$ is then:

$P_1A = \hat{A}$

say $A$ is $\begin{bmatrix} 1, 2 // 3, 4 \end{bmatrix}$, then swapping the rows would look as:

$\begin{bmatrix} 0, 1 \\ 1, 0 \end{bmatrix} \cdot \begin{bmatrix} 1, 2 \\ 3, 4 \end{bmatrix}$

while if we have another permutation matrix, $P_2$, and we want to swap the columns of $A$, the matmul would typically look as:

$AP_2 = \hat{A}$

$\begin{bmatrix} 1, 2 \\ 3, 4 \end{bmatrix} \cdot \begin{bmatrix} 0, 1 \\ 1, 0 \end{bmatrix}$

For larger matrices, you'd need to identify what is the proper permutation matrix $P$, for the desired permutation of $A$ as $\hat{A}$.

Note that each permutation matrix is [[orthogonal]], it's inverse being equal to it's transpose as $P^{-1} = P^T$
