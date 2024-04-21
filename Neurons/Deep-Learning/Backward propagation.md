#mathematics 

Back propagation updates parameters to a global minima of a given loss function through the calculation of the gradients of a [[loss function]] with respect to specific parameters and an [[update rule]].

The mathematics, in a simplified manner, can be defined as:

$gradient = \frac{∂L}{∂θ}$

$θ = θ - ⍺ * gradient$

The means of how we compute these gradients differentiate in the loss function and activation function we use. The mathematical operations are different when we use the [[sigmoid]] over the [[softmax]] or the [[log loss]] over the [[categorical cross entropy]].[^1]

[^1]: See: [[Mathematics of Backpropagation (Sigmoid and Log Loss)]] or [[Mathematics of Backpropagation (Softmax / ReLU and Categorical Cross Entropy)]]