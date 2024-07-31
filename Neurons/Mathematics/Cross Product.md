To compute the cross product of two vectors, say $\vec{v}$ and $\vec{w}$, you can take the two vectors into a single matrix, add a vector of additional coefficients, and then compute the [[determinant]] of that matrix.

$$ \mathbf{u} = \begin{pmatrix} 2 \\ 3 \\ 4 \end{pmatrix}, \quad \mathbf{v} = \begin{pmatrix} 1 \\ 0 \\ 1 \end{pmatrix} $$ $$ \mathbf{u} \times \mathbf{v} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 2 & 3 & 4 \\ 1 & 0 & 1 \end{vmatrix} $$ $$ \mathbf{u} \times \mathbf{v} = \mathbf{i} \cdot \begin{vmatrix} 3 & 4 \\ 0 & 1 \end{vmatrix} - \mathbf{j} \cdot \begin{vmatrix} 2 & 4 \\ 1 & 1 \end{vmatrix} + \mathbf{k} \cdot \begin{vmatrix} 2 & 3 \\ 1 & 0 \end{vmatrix} $$ $$ \mathbf{i} \cdot \left( (3 \cdot 1) - (4 \cdot 0) \right) = \mathbf{i} \cdot 3 $$ $$ - \mathbf{j} \cdot \left( (2 \cdot 1) - (4 \cdot 1) \right) = \mathbf{j} \cdot 2 $$ $$ + \mathbf{k} \cdot \left( (2 \cdot 0) - (3 \cdot 1) \right) = \mathbf{k} \cdot (-3) $$ $$ \mathbf{u} \times \mathbf{v} = 3\mathbf{i} + 2\mathbf{j} - 3\mathbf{k} $$
$$
u \times v = \begin{bmatrix} 3 \\ 2 \\ 3 \end{bmatrix}
$$



The resulting vector, removing the additional coefficients, will then be a vector that is [[orthogonal]] to the plane containing the two original vectors.

It's magnitude can then be defined as:

$|\vec{v}||\vec{w}|sin(\theta)$ where $sin(\theta)$ is the angle between the two vectors.

The area of the parallelogram spanned by two vectors is indeed denoted by the magnitude of their cross product.

Properties:
- If the two vectors are parallel, the cross product will be $0$.
- Not commutative, switching the position of the vectors will invert the sign