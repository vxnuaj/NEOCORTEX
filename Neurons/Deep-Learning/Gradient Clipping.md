Gradient Clipping can be a means to mitigate the risk of exploding gradients, through *clipping* larger values of a gradient vector or matrix, it's clipping threshold being denoted by a variable $k$.

This can be done through **value clipping** and **norm clipping**.

**Value clipping** involves ridding of any value which is larger than $k$, from the original gradient vector / matrix.

$clip(\frac{∂L∂\theta}{∂\theta}, k)$

It's pretty simple and straightforward.

But a disadvantage of gradient clipping is that it can change the direction of the gradient of the given vector or matrix, which may cause training instability, as the updates might not be fully representative of the true gradient.

This is as some values of the gradient along the $y$ axis, that is $∂y$, might be larger than valy

A means to mitigate this is to use **norm clipping**, where the gradients  