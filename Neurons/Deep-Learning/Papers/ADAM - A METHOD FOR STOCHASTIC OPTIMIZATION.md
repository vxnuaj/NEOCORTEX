
> *[Paper](https://arxiv.org/pdf/1412.6980)*

**Intro**

- Gradient descent is an effective means for optimization central to success in machine learning / deep learning. 
- Yet there may be scenarios in which objective functions have sources of high noise, in cases where we need optimization techniques to mitigate these stochastic sources of noise.
- Such a scenario is [[Dropout]] regularization, where you introduce random noise due to the dropout of a random set of neurons.

- So Adam is used as a means to reduce the impact of this noise, to optimize the learning path
- Adam scales the step size of the parameters ($\alpha \cdot \frac{v_i}{\sqrt{s_i + eps}}$) based on the exponentially moving average of the past squared gradients, helping the algorithm and the learning path, be more smooth instead of oscillating widely.

- Adam can handle non stationary objective functions, making models with changing data distributions easier to train.
- Adam can also work well with sparse gradients, given that it averages the gradients rather than taking them at a given time step, $t$
- Adam scales the gradients based on the variability (second moment) to avoid random oscillations and adds momentum (first moment, the moving average of the gradients)
- It then performs step size annealing (scheduling) by reducing the step size as the first and second moment increase.

**Algorithm**

![[Screenshot 2024-06-12 at 9.32.54 AM.png | 500]]

If $f(\theta)$ is the noisy loss function, we're attempting to minimize the value of the loss w.r.t to $\theta$, hence reducing the original loss value thereby increasing model prediction accuracy.

> _The stochastic (random) nature might come from mini-batches or dropout, or other function noise_

So the algorithm computes the exponentially moving averages of the gradients, $m_t$ and the exponentially moving averages of the squared gradients, $v_t$.

- $m_t$ can be known to be the mean of the gradient
- $v_t$ can be known as the uncentered variance of the gradients.
- $\beta_1$ and $\beta_2$ can be known as the parameters that calculate the exponential decay rate of the moving averages

But the moving averages may be initialized to $0$, making them biased towards $0$ during initial time steps.

This can be mitigated through a bias correction, which is a division of the first / second moment term by $(1 - \beta)$.

Adam is defined as:

- Computing the first moment (exponentially weighted average of gradients): 
	- $m_t = \beta m_{t-1} + (1 - \beta) \frac{∂J(\theta)}{∂\theta}$
- Bias correcting the first moment: 
	- $\frac{m_t}{(1 - \beta^t)}$
- Computing the second moment (exponentially weighted average of the squared gradients)
	- $v_t = \ beta(v_{t-1} + (1 - \beta)(\frac{∂J(\theta)}{∂\theta})^2$
- Bias correcting the second moment:
	- $\frac{v_t}{1 - \beta^t}$
- Adam's update rule:
	- $\theta = \theta - \alpha(\frac{m_t}{\sqrt{v_t + \epsilon}})$

Within Adam's update rule, the effective step size, $\alpha(\frac{m_t}{\sqrt{v_t + \epsilon}})$, 