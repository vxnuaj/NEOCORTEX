In matrix spaces, the $\mathbb{R}^n$ of a matrix space is given by the number of unique / independent components in the given matrix.

For example, in a $3 \times 3$ matrix $M$, the dimension is $n = 9$.

But if $M$ is symmetric, it's only independent components are the $3$ in the diagonal, and the $3$ off diagonal values.

Despite there being $6$ off diagonal elements, only $3$ values are independent, as $1$ of them determines the other.

So the dimension of the matrix space, $M$, is $6$ rather than $9$.

Of a given system of equations comprised of matrices, you can solve for independence by vectorizing each matrix into column vectors and then performing row reduction to find the dependent rows and columns.
