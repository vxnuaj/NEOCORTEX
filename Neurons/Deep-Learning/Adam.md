Adam is an extended version of [[Gradient Descent]], designed to improve training speeds in deep neural networks and converge quickly, making use of [[Gradient Descent with Momentum]] and [[RMSprop]], combined.

To compute Adam,

1. Compute the velocity term using the algorithm, $V_{d\theta }= (\beta V_{d\theta - 1}) + (1 - \beta) d\theta$
2. Implement bias correction to the velocity term, $\frac{V_d\theta}{1 - \beta}$
3. Compute the moving average of the accumulated squared gradients using the algorithm, $S_{d\theta} = (\betaS_{d\theta - 1})




---
**Tentative Plan:**

> *Definitely read the paper, take notes, and understand it.*

- [ ] Go over Andrew NGs Interpretation
- [ ] Go over Sebastian Raschka's interpretation
- [ ] Go over Deep Learning Book / Understanding deep learning interpretation
- [ ] Read the Paper
- [ ] Implement it

