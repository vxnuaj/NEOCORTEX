Forward propagation is the feeding forward an input sample into a neural network to get a final prediction based on that same input.

The mathematics, in the case of 2 layer neural network, is defined as:

***First layer:***

$Z^1 = W^1X + B^1$[^1]
$A^1 = g(Z^1)$

***Second layer:***

$Z^2 = W^2A^1 + B^1$[^1]
$A^2 = g(Z^2)$
$\hat{y} = A^2$

where,

- $W^j$ is the weighted matrix at $jth$ layer
- $B^j$ is the bias column vector at $jth$ layer
- $Z^j$ is the weighted sum at $jth$ layer
- - $g()$ is the activation function of the model.
- $A^j$ is the activation matrix from the $jth$ layer

[^1]: You might need to transpose $W$ depending on how you initialize the shape of the matrix or the shape of your input, $X$ / $A^1$


