In Dual Form [[Support Vector Machine]]s, we have to maximize the value of the lagragian as:

$W(\alpha) = \sum_{i=1}^{m} \alpha_i - \frac{1}{2} \sum_{i,j=1}^{m} \alpha_i \alpha_j y_i y_j K(\mathbf{x}_i, \mathbf{x}_j)$

> Where $K(x_i, x_j)$, when using the [[Kernel Trick]], if the [[Kernel Function]].
> Note that the dual form inherently uses the [[Kernel Trick]].

where the constraints are that $\alpha_i > 0$ and $\sum_{i=1}^m a_iy_i = 0$

$W(\alpha)$ aims to maximize the margin $\alpha_i$ and minimizing the error $\sum_{i = 1}^m a_iy_i$

Then for inference, the operation looks as:

$f(u) = \sum_{i = 1}^m \alpha_iy_i K(x_i , u) + b$

where 
- $u$ is the unknown input vector
- $x_i$ are the training samples or support vectors
- $\alpha_i$ are the [[Lagrange Multiplier]] 
- $y_i$ are the class labels for the training examples of $-1$ or $1$
- $b$ is the bias term.

Fitting it all together:

1. Compute the Lagrangian: $W(\alpha) = \sum_{i=1}^{m} \alpha_i - \frac{1}{2} \sum_{i,j=1}^{m} \alpha_i \alpha_j y_i y_j K(\mathbf{x}_i, \mathbf{x}_j)$
2. 