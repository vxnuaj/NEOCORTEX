Gradient descent is an optimization algorithm commonly used in neural networks which involves [[forward propagation]] to get the prediction of a model, [[Back propagation]] to get the gradients of a model, and then an [[update rule]] to optimize the parameters of a model through a [[learning rate]] for a specific number of epochs to the global minima of a [[loss function]].

For example, let's say we have a simple logistic regression model with 3 inputs, hence we have 3 weight parameters and one bias parameter

- The weight matrix is defined as $W$ and the bias matrix is defined as $B$.
- The loss function is defined as $L$
- The activation output is defined as $A$
- The weighted sum is defined as $Z$

Gradient descent for updating the weights of this model would mathematically look as:

$A = σ(W · X + B)$

$L = -Y*log(A) - (1 - Y)*log(1 - A)$

$\frac{∂L}{∂W} = (\frac{∂L}{∂A})(\frac{∂A}{∂Z})(\frac{∂Z}{∂W})$

$W = W - ⍺ * \frac{∂L}{∂W}$

while the gradient descent for updating the bias would look as:

$A = σ(W · X + B)$

$L = -Y*log(A) - (1 - Y)*log(1 - A)$

$\frac{∂L}{∂B} = (\frac{∂L}{∂Z})(\frac{∂Z}{∂B})$

$B = B - ⍺ * \frac{∂L}{∂B}$

