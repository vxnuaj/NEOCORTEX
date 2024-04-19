#mathematics 

Back propagation updates parameters to a global minima of a given loss function through the calculation of the gradients of a [[loss function]] with respect to specific parameters and an [[update rule]].

Mathematically, given a neural network of one output layer and one hidden layer, this might looks as:

> *If we use [[Log Loss]] as our [[loss function]]*

***Output layer:***

$\frac{∂L}{∂Z_2} =  (\frac{∂L}{∂A_2})(\frac{∂A_2}{∂Z_2}) = A - Y$

$\frac{∂L}{∂W_2} = (\frac{∂L}{∂A_2})(\frac{∂A_2}{∂Z_2})(\frac{∂Z_2}{∂W_2}) = X (A - Y)$[^1]

$\frac{∂L}{∂B_2} = (\frac{∂L}{∂Z_2})(\frac{∂Z_2}{∂B_2}) = A - Y$[^2]

> $\frac{∂Z}{∂B_2}$ is $0$ given that $B$ is a constant, hence we get $A - Y$ for $\frac{∂L}{∂B_2}$

$W = W - ⍺(\frac{∂L}{∂W_2})$

$B = B - ⍺(\frac{∂L}{∂B_2})$

***Hidden layer:***

$\frac{∂L}{∂Z_1} = (\frac{∂L}{∂A_2})(\frac{∂A_2}{∂Z_2})(\frac{∂Z_2}{∂A_1})(\frac{∂A_1}{∂Z_1}) = W \frac{∂L}{∂Z_2} * \frac{∂L}{∂A_1}$ 

$\frac{∂L}{∂W_1} = (\frac{∂L}{∂Z_1})(\frac{∂Z_1}{∂W_1}) = \frac{∂L}{∂Z_1}X$ 

$\frac{∂L}{∂B_1} = (\frac{∂L}{∂Z_1})(\frac{∂Z_1}{∂B_1}) = W \frac{∂L}{∂Z_2} * \frac{∂L}{∂A_1} = \frac{∂L}{∂Z_1}$

[^1]:  The $(\frac{∂L}{∂A_2})(\frac{∂A_2}{∂Z_2})$ is equivalent to $A - Y$ (given by $\frac{∂L}{∂Z_2}$) and the $\frac{∂Z_2}{∂W_2}$ is equivalent to $X$ given that in the original linear combination, the multiplication of $W \cdot X$ is equal to $Z$.

[^2]: The $\frac{∂L}{∂B_2}$ is equivalent to $A - Y$ as $(\frac{∂L}{∂A_2})(\frac{∂A_2}{∂Z_2}) = \frac{∂L}{∂Z_2} = A - Y$ and $(\frac{∂Z_2}{∂B_2})$ yields $0$ given that $B$ is a constant in the linear combination of $W \cdot X + B$