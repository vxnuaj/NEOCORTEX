#mathematics 

Back propagation updates parameters to a global minima of a given loss function through the calculation of the gradients of a [[loss function]] with respect to specific parameters and an [[update rule]].

Mathematically, given a neural network of one output layer and one hidden layer, this might looks as:

> *If we use [[Log Loss]] as our [[loss function]]*

*Output layer:*

$\frac{∂L}{∂Z} =  (\frac{∂L}{∂A})(\frac{∂A}{∂Z}) = A - Y$

$\frac{∂L}{∂W} = (\frac{∂L}{∂A})(\frac{∂A}{∂Z})(\frac{∂Z}{∂W}) = X (A - Y)$

$\frac{∂L}{∂B} = (\frac{∂L}{∂Z})(\frac{∂Z}{∂B}) = A - Y$ 

> $\frac{∂Z}{∂B}$ is $0$ given that $B$ is a constant, hence we get $A - Y$ for $\frac{∂L}{∂B}$

$W = W - ⍺(\frac{∂L}{∂W})$

$B = B - ⍺(\frac{∂L}{∂B})$

*Hidden layer:*

$\frac{∂L}{∂W} = (\frac{∂L}{∂A})(\frac{∂A}{∂Z})(\frac{∂Z}{∂A})(\frac{∂A}{∂Z})\frac{∂Z}{∂}$