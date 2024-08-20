#LinearAlgebra #stats 

A Covariance matrix for given vectors, $X$ and $Y$:

$X = \begin{bmatrix} 2, 4, 6, 8 \end{bmatrix}$
$Y = [5, 9, 7, 10]$ 

is found as:

$$
\bar{X} = \frac{2 + 4 + 6 + 8}{4} = 5, \quad \bar{Y} = \frac{5 + 9 + 7 + 10}{4} = 7.75
$$
$$
\text{Cov}(X, X) = \frac{1}{n-1} \sum_{i=1}^{n} (X_i - \bar{X})^2 
= \frac{1}{3} \left[(2 - 5)^2 + (4 - 5)^2 + (6 - 5)^2 + (8 - 5)^2 \right]
= \frac{1}{3} \left[9 + 1 + 1 + 9 \right] = \frac{20}{3} \approx 6.67
$$
$$
\text{Cov}(X, Y) = \frac{1}{n-1} \sum_{i=1}^{n} (X_i - \bar{X})(Y_i - \bar{Y}) 
= \frac{1}{3} \left[(2 - 5)(5 - 7.75) + (4 - 5)(9 - 7.75) + (6 - 5)(7 - 7.75) + (8 - 5)(10 - 7.75) \right]
= \frac{13}{3} \approx 4.33
$$
$$
\text{Cov}(Y, Y) = \frac{1}{n-1} \sum_{i=1}^{n} (Y_i - \bar{Y})^2 
= \frac{1}{3} \left[(5 - 7.75)^2 + (9 - 7.75)^2 + (7 - 7.75)^2 + (10 - 7.75)^2 \right]
= \frac{14.75}{3} \approx 4.92
$$
$$
\text{Covariance Matrix} = \begin{bmatrix} 
\text{Cov}(X, X) & \text{Cov}(X, Y) \\
\text{Cov}(Y, X) & \text{Cov}(Y, Y) 
\end{bmatrix} = \begin{bmatrix} 
6.67 & 4.33 \\
4.33 & 4.92 
\end{bmatrix}
$$
Covariance Matrix is symmetric, it's transpose is equal to the original matrix

