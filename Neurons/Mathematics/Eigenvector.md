#LinearAlgebra 

An Eigenvector of a matrix $A$, is any vector $\vec{x} \in \mathbb{R}$ where $\vec{x} ≠ \vec{0}$  that when multiplying a matrix $A$ by $\vec{x}$ you get back a scalar multiple of vector $\vec{x}$ where the multiplier of $x$ is $\lambda$, which $\in \mathbb{R}$.

> *The scalar multiplier, $\lambda$, is called the [[eigenvalue]]*

1. $A\vec{x} = \lambda\vec{x}$
2. $A\vec{x} = \lambda I\vec{x}$
3. $A\vec{x} - \lambda I \vec{x} = 0$
4. $\vec{x}(A - \lambda I) = 0$
5. $det(A - \lambda I ) \rightarrow polynomial$
6. $polynomial_{root} \rightarrow eigenvalue \hspace{1mm} (\lambda)$
7. Plug $\lambda$ back into $A\vec{x} = \lambda \vec{x}$ and solve the system of equations to get the eigenvectors
8. Verify answer.

$A\vec{x} = \lambda\vec{x}$

where:

- $\vec{x} ≠ \vec{0}$
- $\lambda \in \mathbb{R}$

Note that for an Eigenvector to exist, $det(A - \lambda I)$ must equal $0$