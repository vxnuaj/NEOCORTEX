
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
- It then performs step size annealing (scheduling) by reducing the step size 