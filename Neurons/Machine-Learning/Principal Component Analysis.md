Principal Component Analysis is the means for reducing the dimensionality of a dataset, say ${X_k}, k \in [1, ..., N]$ with dimensionality $D$ to dimensionality $M$ where $M < D$.

Essentially, it answers, *"How do we reduce the dimensionality of a set of samples?"*.

It aims to maximize the preservation of the original variation of $x_k$ with dimensionality $D$, while compressing $x_k$ down to dimensionality $M$, again where $M < D$.

PCA wants to find the direction at which the variance has the maximum direction.

If $V$ is a principal component, the variance of dataset $X$ projected onto $V$ is given as:

$Variance = \frac{1}{N} \sum_{k=1}^N(V^TX_k - V^T\bar{X})^2$
$Variance = V^T(\frac{1}{N} \sum_{k=1}^N(X_k - \bar{X})(X_k - \bar{X})^T)V$
$Variance = V^TCV$

where $C$ turns to be the covariance matrix.

We want to maximize $V^TCV$ subject to $||V|| = 1$

This is done through [[Lagrange Multiplier]]s, $\mathcal{L}(x, \lambda)= f(x) + \lambda g(x)$, where $g(x)$ is the constraint, $1 - ||V||$,and $f(x)$ is the function we want to maximize, in this case the variability of the projection $V$ onto $X$, $f(x) = V^TCV$.

$\mathcal{L}(x, \lambda)= V^TCV + \lambda (1 - ||V||)$

We take the derivative as:

$\frac{∂\mathcal{L}}{∂v} = 2CV - 2\lambda V$

and then simplify to:

$2CV = 2\lambda V$
$CV = \lambda V$ (eigenvector / value problem)
$CV = \lambda I V$, where $I$ is the identity matrix.
$CV - \lambda IV = 0$
$V (C - \lambda I) = 0$

Where now we want to find the $det()$ of $C - \lambda I$, which will result in a polynomial.

We then find the roots of this polynomial to find the largest eigenvalue ($\lambda$) which corresponds to the [[Lagrange Multiplier]] that maximizes the the variability of the projected data whilst having the constraint of $||V|| = 1$.

This [[Lagrange Multiplier]] is used to then find the eigenvector which serves as the principal component $(P)$ for reducing the dimensionality of the original data vector, $X_k$

To reduce it, all we do is apply a [[Vector Projection]] as:

$K = \frac{XP}{||P||^2}$ 
$X_{kPCA} = PK$ 

where $K$ is the multiple of the principal component $P$ that represents the 

We want to maximize the variance,

1. Finding the mean of $X$, $\bar{X}$
2. Mean centering $X$ as $X = X - \bar{X}$
3. Compute the covariance matrix of $X$ as $S = \frac{1}{N - 1} \sum_{k=1}^N (x_k - \bar{x})(x_k - \bar {x})^T$
5. Find the Lagrange multipliers of $S$, ones that maximize the variability subject to the eigenvectors, $.
6. Find the eigenvalues of $S$.
7. Use the eigenvalues, $S$, to solve for the eigenvectors

Principal Component Analysis is useful for:
1. Dimensionality Reduction
2. Data Visualization
3. Feature Extraction