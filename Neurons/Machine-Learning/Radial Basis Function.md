The radial basis function computes the similarity between two given datapoints, based on their distance.

$K(x, y) = e^{-\frac{||x - y||^2}{2\sigma^2}}$

where:
- $||x - y||$ is the [[Euclidean Distance]] between $x$ and $y$
- $\sigma$ is the parameter that controls the width of the gaussian function.

The kernel value, $K$, decreases as the distance between $x$ and $y$ increases, indicating that they aren't similar.

Inversely, a higher similarity yields a higher $K$.

As $\sigma$ decreases, the similarity measure becomes less sensitive to distance, points that are further apart will still have higher similarity scores compared to when $\sigma$ is a lower value.

The $\Delta$ of the exponential decay in the RBF kernel will be lower when $\sigma$ is smaller, and conversely, higher when $\sigma$ is larger.