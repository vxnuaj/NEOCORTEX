#stats 

Covariance measures how much 2 variables change together, quantifying the degree to which changes in 1 variable, $X$, are correlated with the same changes in $Y$.

$Cov_{population}(X, Y) = \frac{1}{N} \sum_{i=1}^N (X_i - \mu_X)(Y_i - \mu_Y)$
$Cov_{sample}(X, Y) = \frac{1}{n-1} \sum_{i=1}^n (X_i - \mu_X)(Y_i - \mu_Y)$


If $X$ and $Y$ are both extremely positive or extremely negative, then they have a high degree of covariance.

Otherwise, if $X$ is extremely positive and $Y$ is extremely negative, they have a very low covariance.

The covariance of a variable with itself, say $X$ as $Cov(X, X)$ is simply $Var(X)$.