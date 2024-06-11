Nesterov momentum is an alternative to traditional [[Momentum]], acting as another term that can push a model out of saddle points of the loss during [[gradient descent]].

Nesterov momentum varies from regular [[momentum]] by considering the gradient, not at the current position but at a slightly looked ahead position.

This then informs the weight update by taking a look at a predicted position of parameters rather than the parameters are their current value.

Nesterov momentum is defined as:

	$dw = \sum \frac{∂L(\theta - \alpha\beta \cdot vdw)}{∂\theta}$
	
	$vdw = \beta vdw + (1 - \beta)dw \cdot \alpha$
	
	$w = w - vdw$

or with the $\alpha$ value outside of the computation:

	$dw = \sum \frac{∂L(\theta - \beta \cdot vdw)}{∂\theta}$
	$vdw = \beta vdw + (1 - \beta)dw$
	$w = w - \alpha \cdot vdw$
