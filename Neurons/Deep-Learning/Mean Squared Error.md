The mean squared error is a type of [[loss function]] that measure the amount of error in statistical models, such as a [[linear regression]] model.

The formula is given as such:

$MSE = \frac{1}{n} \sum_{i=1}^{n}(y_i - \hat{y}_i)^2$,

where $n$ is the total number of samples in a dataset and $i$ is the index of the $ith$ sample in the range of $1 ≤ i ≤ n$.

The MSE assesses the average *squared difference* between a predicted value and a true value.

When a model has no error or difference between the prediction and the true value, the value of the MSE is 0. As the error or difference increases, the MSE begins to increase proportionally.

Squaring the differences is less intuitive to interpret but makes sure to eliminate any negative values for difference and ensures that the MSE is always equal to or greater than 0. It also punishes larger errors allowing for improved convergence through [[gradient descent]].