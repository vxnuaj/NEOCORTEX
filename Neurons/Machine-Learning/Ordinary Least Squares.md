Ordinary Least Squares is a means to finding the optimal parameters in a linear regression, through simple equations which rely on mean centering as:

$\hat{\beta}_1 = \frac{\sum_{i=1}^n (x_i - \bar{x})(y_i - \bar{y})}{\sum_{i=1}^n (x_i - \bar{x})^2}$

$\hat{\beta}_0 = \bar{y} - \hat{\beta}_1\bar{x}$

where any variable denoted by $\bar \theta$ is it's mean.

If the datapoints $x$ or $y$ are already 0 centered as 0 being the mean, you don't need to take the mean of them prior to computing the equation and can just go ahead without as:

$\hat{\beta}_1 = \frac{\sum_{i=1}^n x_i y_i}{\sum_{i=1}^n x_i^2}$

$\hat{\beta_0} = 0$

