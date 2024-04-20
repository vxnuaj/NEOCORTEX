#mathematics 

Back propagation updates parameters to a global minima of a given loss function through the calculation of the gradients of a [[loss function]] with respect to specific parameters and an [[update rule]].

Mathematically, given a neural network of one output layer and one hidden layer, this might looks as:

> *If we use [[Log Loss]] as our [[loss function]]*

***Output layer:***

$\frac{∂L}{∂Z_2} =  (\frac{∂L}{∂A_2})(\frac{∂A_2}{∂Z_2}) = A_2 - Y$

$\frac{∂L}{∂W_2} = (\frac{∂L}{∂A_2})(\frac{∂A_2}{∂Z_2})(\frac{∂Z_2}{∂W_2}) = A_1^T (A_2 - Y)$[^1]

$\frac{∂L}{∂B_2} = (\frac{∂L}{∂Z_2})(\frac{∂Z_2}{∂B_2}) = A_2 - Y$[^2]

> *$\frac{∂Z}{∂B_2}$ is $1$ given that $B$ is an isolated value, hence we get $A - Y$ for $\frac{∂L}{∂B_2}$*

$W = W - ⍺(\frac{∂L}{∂W_2})$

$B = B - ⍺(\frac{∂L}{∂B_2})$

***Hidden layer:***

$\frac{∂L}{∂Z_1} = (\frac{∂L}{∂A_2})(\frac{∂A_2}{∂Z_2})(\frac{∂Z_2}{∂A_1})(\frac{∂A_1}{∂Z_1}) = W_2 \frac{∂L}{∂Z_2} * \frac{∂L}{∂A_1}$ 

$\frac{∂L}{∂W_1} = (\frac{∂L}{∂Z_1})(\frac{∂Z_1}{∂W_1}) = \frac{∂L}{∂Z_1}X^T$ [^3]

$\frac{∂L}{∂B_1} = (\frac{∂L}{∂Z_1})(\frac{∂Z_1}{∂B_1}) = W_1 \frac{∂L}{∂Z_2} * \frac{∂L}{∂A_1} = \frac{∂L}{∂Z_1}$[^4]

In a real implementation for a neural network, you'd need to average out the gradients of the loss w.r.t $W$ by dividing over $m$ samples and $B$ by taking the summation and dividing over $m$ samples. 

The reason we don't taking the summation when calculating $\frac{∂L}{∂W}$ is due to the fact that the dot product already implicitly calculates a summation[^5].

[^1]:  The $(\frac{∂L}{∂A_2})(\frac{∂A_2}{∂Z_2})$ is equivalent to $A - Y$ (given by $\frac{∂L}{∂Z_2}$) and the $\frac{∂Z_2}{∂W_2}$ is equivalent to $X$ given that in the original linear combination, the multiplication of $W \cdot X$ is equal to $Z$.

[^2]: The $\frac{∂L}{∂B_2}$ is equivalent to $A - Y$ as $(\frac{∂L}{∂A_2})(\frac{∂A_2}{∂Z_2}) = \frac{∂L}{∂Z_2} = A - Y$ and $(\frac{∂Z_2}{∂B_2})$ yields $1$ given that $B$ is a constant in the linear combination of $W \cdot X + B$. The bias, $B$, then gets updated based on $\frac{∂L}{∂Z}$.

[^3]:  The $(\frac{∂Z_1}{∂W_1})$ is equal to $X$ as the multiplication of input $X$ by $W_1$ is what yields $Z_1$, hence the derivative is $X$

[^4]: Similarly to footnote 2,[^2],  $(\frac{∂Z_1}{∂B_1})$ will yield 1 hence the $\frac{∂L}{∂B_1}$ is determined by $\frac{∂L}{∂Z_1}$ and $B$ is updated by $\frac{∂L}{∂Z_1}$

[^5]: This is to the best of my knowledge, though there's a significant chance I'm wrong. What I know for certain is that we don't take the summation, but my reasoning behind it might be fallible. I need to learn the linear algebra.