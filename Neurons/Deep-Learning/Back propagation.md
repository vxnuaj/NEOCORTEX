#mathematics 

Back propagation updates parameters to a global minima of a given loss function through the calculation of the gradients of a [[loss function]] with respect to specific parameters and an [[update rule]].

The mathematics, in the case of a 2 layer network, is defined as:

> *Using the [[sigmoid]] activation function and [[log loss]] function*

***First Layer:***

$\frac{∂J}{∂Z_2} = (\frac{∂J}{∂A_2})(\frac{∂A_2}{∂Z_2}) = A_2 - Y$

$\frac{∂J}{∂W_2} = (\frac{∂J}{∂A_2})(\frac{∂A_2}{∂Z_2})(\frac{∂Z_2}{∂W_2}) = \frac{1}{m} A_1^T(A_2 - Y)$ [^1] [^2]

$\frac{∂J}{∂B_2} = \frac{1}{m}\sum_{i=1}^m(\frac{∂J}{∂A_2})(\frac{∂A_2}{Z_2})(\frac{∂Z_2}{B_2}) =  \frac{1}{m}\sum_{i=1}^m A_2 - Y$  

***Second Layer:***

$\frac{∂J}{∂Z_1} = (\frac{∂J}{∂A_2})(\frac{∂A_2}{∂Z_2})(\frac{∂Z_2}{∂A_1})(\frac{∂A_1}{∂Z_1}) = W_2 \frac{∂L}{∂Z_2} * \frac{∂J}{∂A_1}$

$\frac{∂J}{∂W_1} = (\frac{∂J}{∂Z_1})(\frac{∂Z_1}{∂W_1}) = \frac{∂J}{∂Z_1}X^T$

$\frac{∂J}{∂B_1} = (\frac{∂J}{∂Z_1})(\frac{∂Z_1}{∂B_1}) = W_2 \frac{∂J}{∂Z_2} * \frac{∂J}{∂A_1} = \frac{∂J}{∂Z_1}$
---


[^1]:  The $(\frac{∂J}{∂A_2})(\frac{∂A_2}{∂Z_2})$ is equivalent to $A - Y$ (given by $\frac{∂L}{∂Z_2}$) and the $\frac{∂Z_2}{∂W_2}$ is equivalent to $A_1^T$ given that in the original linear combination, the multiplication of $W \cdot X$ is equal to $Z$. We take the transpose of $A$ to ensure that the dimensions of $A$ align for the matrix multiplication of the computation.

[^2]: We average the loss over $\frac{1}{m}$ to normalize the gra