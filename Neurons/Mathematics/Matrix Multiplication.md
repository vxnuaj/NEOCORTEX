#LinearAlgebra 

A matrix multiplication is a multiplication by 2 matrices, where each row of the first matrix corresponds to the [[Dot Product]] of each column in the second matrix.

**Example 1**

$\begin{pmatrix}a_{11}, a_{12}\\ a_{21}, a_{22}\end{pmatrix} \cdot \begin{pmatrix} b_{11}, b_{12}\\ b_{21}, b_{22} \end{pmatrix} = C$

$C = \begin{pmatrix} a_{11} \cdot b_{11} + a_{12} \cdot b_{21} & a_{11} \cdot b_{12} + a_{12} \cdot b_{22} \\ a_{21} \cdot b_{11} + a_{22} \cdot b_{21} & a_{21} \cdot b_{12} + a_{22} \cdot b_{22} \end{pmatrix}$


A matrix multiplication of $A$ with shape $m, n$ and $B$ of shape $n, m$ can transform $B$ from $\mathbb{R}^n$ to $\mathbb{R}^m$.

As another example:

$AB = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix} \begin{pmatrix} 2 & 4 \\ 1 & 3 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 4 & 16 \\ 14 & 38 \end{pmatrix}$

The matrix $B$ is of dimensions $\mathbb{R}^{3x2}$ while matrix $A$ is of dimensions $\mathbb{R}^{2x3}$. 

When applying the linear combination, the matrix $B$ is transformed by $A$ to get output $C$ which has the dimensionality of $m, m$. 

Thereby the output of a matrix multiplication is a dimensionality of the rows of the first matrix and the columns of a second matrix.
