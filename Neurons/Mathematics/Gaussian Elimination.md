#todo 

Given a matrix $A$, of:

$A = \begin{pmatrix} 2 & 1 & -1 \\ -3 & -1 & 2 \\ -2 & 1 & 2 \end{pmatrix}$

Choose the leftmost column that doesn't consist of all $0$s.

The topmost row must not have a $0$ as it's first entry. Swap any row to ensure this if needed.

Then, multiply each element of the matrix by a scalar defined by $\frac{1}{a}$, where $a$ is the first element in the first row.

$\begin{pmatrix} 1 & \frac{1}{2} & -\frac{1}{2} \\ -3 & -1 & 2 \\ -2 & 1 & 2 \end{pmatrix}$

Then, add suitable multiples of the first row to the rows below so that all entries below the leading $1$ become $0$.

$\begin{pmatrix} 1 & \frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{2} & \frac{1}{2} \\ 0 & 2 & 1 \end{pmatrix}$

This is repeated for the sub matrices of $A$, until $A$ is in row [[row echelon form]].