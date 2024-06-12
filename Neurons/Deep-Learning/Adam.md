 Adam, *Adaptive moment estimation*, is an extended version of [[Gradient Descent]], designed to improve training speeds in deep neural networks and converge quickly, making use of [[Momentum]] and [[RMSprop]], combined.

[[Gradient Descent]] with a fixed step size has the undesirable property in which it makes large changes to parameters with large gradients and small adjustments to parameters with small gradients.

We might not always want large changes to parameters with large gradients, we might want to be cautious at that point.

We might not always want small changes to parameters with small gradients, we might want to explore the space further and take slightly larger steps.

>_It all depends on the surface of the loss function_

So to compute Adam,

1. Compute the velocity term (1st moment) using the algorithm, $V_{d\theta }= (\beta_1 V_{d\theta - 1}) + (1 - \beta_1) d\theta$

2. Implement a bias correction to the velocity term, $\frac{V_d\theta}{1 - \beta^t}$

3. Compute the moving average of the accumulated squared gradients (2nd moment) using the algorithm, $S_{d\theta} = (\beta_2 S_{d\theta - 1}) + (1 - \beta_2)d\theta^2$

4. Implement a bias correction term, $\frac{S_{d\theta}}{(1 - B_2^t)}$

5. Perform the weight update, $\theta = \theta - \alpha(\frac{V_{d\theta}}{\sqrt{S_{d\theta} + \epsilon}})$, with the small $\epsilon$ value to avoid division by $0$

Then, you have 3 hyperparameters to tune:

1. Learning rate: $\alpha$
2. Momentum Term: $B_1$, typically initialized to $.9$
3. RMSprop Term: $B_2$, authors of the paper recommend to initialize to $.99$

Adam is typically used in mini-batch gradient descent, given an increase in oscillations of the loss and accuracy during, which Adam can help in mitigating.

![[Screenshot 2024-06-12 at 9.01.31 AM.png | 700]]

---

**Tentative Plan:**

> *Definitely read the paper, take notes, and understand it.*

- [x] Go over Andrew NGs Interpretation
- [x] Go over Sebastian Raschka's interpretation
	- [x] Adam
- [x] Go over Deep Learning Book / Understanding deep learning interpretation
- [ ] Read the Paper
- [x] Implement it

