#calculus 

Given a scalar-valued  multivariable function, $f$, the Hessian matrix is the construction of the 2nd order partial derivatives of the function $f$.

Denoted as $H(f)$.

Given a function $f(x_1, ..., x_n)$, the structure of $H(f)$ is as:

$H(f) = \begin{pmatrix} \frac{\partial^2 f}{\partial x_1^2} & \frac{\partial^2 f}{\partial x_1 \partial x_2} & \cdots & \frac{\partial^2 f}{\partial x_1 \partial x_n} \\ \frac{\partial^2 f}{\partial x_2 \partial x_1} & \frac{\partial^2 f}{\partial x_2^2} & \cdots & \frac{\partial^2 f}{\partial x_2 \partial x_n} \\ \vdots & \vdots & \ddots & \vdots \\ \frac{\partial^2 f}{\partial x_n \partial x_1} & \frac{\partial^2 f}{\partial x_n \partial x_2} & \cdots & \frac{\partial^2 f}{\partial x_n^2} \end{pmatrix}$


NOTATION; 

In $\frac{∂^2f}{∂x_m∂x_n}$, we computed $\frac{∂f}{∂x_n}$ first.

The $∂$ w.r.t **right most** term is computed first.

**PROPERTIES**

- The Hessian matrix is symmetric, where $\frac{∂^2f}{∂x_i∂x_j} = \frac{∂^2f}{∂x_i∂x_j}$ , following Schwarz's theorem, where if the second order partial derivatives form a continuous functions, the mixed partials are equal to each other.
- If we don't have an $H(f)$, the function is not differentiable, up to the second order., we dont' have guaranteed information about it's concavity (note that second order derivatives determine the change, of the rate of change. Think acceleration in physics).
- The matrix is always symmetric, an $n\times n$ matrix if $f$ if a function of $n$ variables


---


is the hessian matrix just a matrix of derivatives then? what is the structure like?
