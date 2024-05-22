L2 regularization, as [[Regularization]], involves the addition of a penalty term to punish large weights.;

The penalty term is based on the [[euclidean norm]] squared, multiplied by a hyperparameter, $\lambda$.

The regularized loss is then calculated as:

$J(w,b)_{regularized} = \sum L(\hat{y}, y) + \lambda||w||^2$

This is also known as weight decay, as when doing [[Gradient Descent]], a subset of the parameters will decay to smaller values given the introduction of the small value of $\lambda$.

Then, in [[Gradient Descent]], the implementation of regularized loss looks mathematically as (w.r.t to param $w$, assuming [[Categorical Cross Entropy Loss]]):

$\frac{∂J_{regularized}}{∂w} = (\frac{∂J}{∂Z})(\frac{∂Z}{∂W}) + 2\lambda||w||$

$\frac{∂J_{regularized}}{∂w} = (A - Y_{onehot})(X^T) + 2\lambda||w||$

$w = w - \alpha * \frac{∂J_{regularized}}{∂w}$

>*When computing the loss, you must take the squared euclidean norm of **all** weight matrices, not just only the output layer.*


Essentially, [[overfitting]] requires a set of large weights. An L2 regularized back propagation adds the additional $2\lambda||w||$ term to increase a gradient.

The larger $||w||$ is, the higher the gradient will be, therefore forcing a model to optimize for a narrower set of parameters.


- [x] understand theory + mathematics.
- [ ] implement onto model in numpy