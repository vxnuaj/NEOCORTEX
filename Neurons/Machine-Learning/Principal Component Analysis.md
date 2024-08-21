Principal Component Analysis is the means for reducing the dimensionality of a dataset, say ${x_k}, k \in [1, ..., N]$ with dimensionality $D$ to dimensionality $M$ where $M < D$.

Essentially, it answers, *"How do we reduce the dimensionality of a set of samples?"*.

It aims to maximize the preservation of the original variation of $x_k$ with dimensionality $D$, while compressing $x_k$ down to dimensionality $M$, again where $M < D$.

PCA wants to find the direction at which the variance has the maximum direction.

If $V$ is a principal component, the variance of dataset $X$ projected onto $V$ is given as:

$Variance = \frac{1}{N} \sum_{k=1}^N(V^TX_k - V^T\bar{X})^2$
$Variance = V^T(\frac{1}{N} \sum_{k=1}^N(X_k - \bar{X})(X_k - \bar{X})^T)V$
$Variance = V^TCV$

where $C$ turns to be the covariance matrix.

We want to maximize $V^TCV$ subject to $||V|| = 1$

This is done through 

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