Gradient descent is an optimization algorithm that involves taking the gradients of a [[loss function]] with respect to a specific parameter within a neural network and then using the gradient to update the specific parameter through an [[Update rule]] at a specific [[learning rate]] for a given number of epochs.

For example, let's say we have a simple logistic regression model with 3 inputs, hence we have 3 weight parameters and one bias parameter

- The weight matrix is defined as $W$ and the bias matrix is defined as $B$.
- The loss function is defined as $L$
- The activation output is defined as $A$
- The weighted sum is defined as $Z$

Gradient descent for updating the weights of this model would mathematically look as:

$\frac{∂L}{∂W} = (\frac{∂L}{∂A})(\frac{∂A}{∂Z})(\frac{∂Z}{∂W})$

$W = W - ⍺ * \frac{∂L}{∂W}$

while the gradient descent for updating the bias would look as:

$\frac{∂L}{∂B} = (\frac{∂L}{∂Z})(\frac{∂Z}{∂B})$

$B = B - ⍺ * \frac{∂L}{∂B}$

