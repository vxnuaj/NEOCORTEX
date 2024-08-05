Linear dependence is when a vector or set of vectors can be written as a linear combination of other vectors.

*Linear dependence over row vectors in a system of lin. eq.:*

$\begin{cases} x + y = 2 \\ 2x + 2y = 4 \\ 3x + 3y = 6 \end{cases}$

*Linear dependence over column vectors:*

$A = \begin{pmatrix} 1 & 1 \\ 2 & 2 \\ 3 & 3 \end{pmatrix}$

If we have a vector $\vec{c}$ where it is equal to the linear combination of $\vec{a} + 2\vec{b}$, $\vec{c}$ would be considered to be linearly dependent on $\vec{a} + 2\vec{b}$.

A vector is then linearly independent if it can't be expressed as a linear combination of a given set of vectors.

It is not possible for a vector to be linearly independent amongst all possible vectors in a vector space

In terms of [[Linear Combination]]s, as long as all columns $A$ are linearly independent, we can map any vector within $Col(A)$[^1] that's $\in \mathbb{R}^m$, if $A$ is dimensions $m, n$.

If we have the linear combination, $A\vec{x} = 0$, meaning a homogeneous system, and $\vec{x}$ is non-zero, therefore $A$ is linearly dependent and not full rank.


[^1]: [[Column Space]]Space]]
