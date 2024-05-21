L2 regularization, as [[Regularization]], involves the addition of a penalty term to punish large weights.;

The penalty term is based on the [[euclidean norm]] squared, multiplied by a hyperparameter, $\lambda$.

$J(w,b)_{regularized} = \sum L(\hat{y}, y) + \lambda||w||^2$

This is also known as weight decay, as when doing [[Gradient Descent]], a subset of the parameters will decay to smaller values given the introduction of the small value of $\lambda$.

Then, in [[Gradient Descent]], the implementation of regularized loss looks mathematically as (w.r.t to param $w$, assuming [[Categorical Cross Entropy Loss]]):

$\frac{∂J_{regularized}}{∂w} = (\frac{∂J}{∂Z})(\frac{∂Z}{∂W}) + 2\lambda||w||$

$\frac{∂J_{regularized}}{∂w} = (A - Y_{onehot})(X^T) + 2\lambda||w||$

- [ ] understanding the weight update and write it.
