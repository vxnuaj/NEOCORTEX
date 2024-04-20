#mathematics 

As an example, say we had a neural network of one hidden layer, and an output layer of one sample.

$w^1$, of dims $(n^1, n^0)$
$b^1$, of dims $(n^1, 1)$
$w^2$, of dims $(n^2, n^1)$ or $(1, n^1)$
$b^2$, of dims $(n^2, 1)$ or $(1, 1)$ 

where,

$n_x = n^0$, corresponding to total input features.
$n^1$, corresponding to number of neurons in hidden layer.
$n^2 = 1$, corresponding to number of neurons in the output layer

and the [[cost function]], defined as $J$ is:

$J(w^1, b^1, w^2, b^2) = \frac{1}{m}\sum_{i=1}^{m}L(\hat{y}, y)$

