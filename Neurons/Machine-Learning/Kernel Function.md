A kernel function is a mapping function that allows us to map an input vector $x$ in $\mathbb{R}^n$ onto a higher dimensional space.

It can be seen as:

$K(x, x') = \phi(x)^T \phi(y)$

where $\phi$ is a transformation that maps a vector into a higher dimensional space. Then $\phi(x)$ and $\phi(y)$ are $x$ and $y$ in a higher dimensional space.

The output of this kernel function is a scalar value representing the inner product of 2 input vectors in an $nth$ dimension defined by the kernel.

The kernel trick allows for us to compute $\phi(x)$ and $\phi(y)$ without explicitly knowing what $\phi$ is or computing it directly and without knowing which $n$th dimensional space to project to.

The output of this kernel function, say $K$, takes the place of input data, $X$, to be fed into the SVM.