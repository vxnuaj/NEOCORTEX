You can typically normalize the inputs to a neural network by applying [[Z-Score Normalization]] or another means of a simply division by $255$ for pixel values.

This works well for input features.

But, in deeper networks, you might also want to normalize the input features into each layer.

This is what [[Batch Normalization]] does.

We can normalize the linear transformation $(z_{l}$) to a scale that's more easily computable by a deep neural network.

> *Typically, its seems that batch normalization is applied prior to the activation function, after the linear transformation, though doing after the activation can work as well.* 

Batch Normalization can then be applied per layer to the weighted sum, $z_l$.

$\mu = \frac{1}{m} \sum_{i=1}^m Z_l^i$, where $m$ is the number of input neurons to the following layer.
	
$Z_l^i = Z_l^i - \mu$

$\sigma^2 = \frac{1}{m} \sum_{i = 1}^m (Z_l^i - \mu)^2$, where $m$ is the number of input neurons to the following layer.

$Z_{lnorm} = \frac{Z_l}{\sqrt{\sigma^2 + \epsilon}}$

The mean and variance of the $Z_{norm}$ can be trained through parameters $\gamma$ and $\beta$.

$\tilde{Z_{lnorm}^i} = \gamma Z_{lnorm}^i + \beta$

$\gamma$ is known as the scale parameter, which can be used to scale the normalized value It can either amplify or dampen the scale of $Z_{lorm}$ based on what's more beneficial for model performance

$\beta$ is the parameter to shift the distribution of the normalized values, to better fit the desired output distribution to optimize model performance.

The $\gamma$ and $\beta$ parameters should be matrices of same dimensions as output $Z^l$.

> *These aren't [[Hyperparameters]], but instead learnable parameters during [[gradient descent]]*.

Of course if $\gamma = \sqrt{\sigma^2 + \epsilon}$ and $\beta = \mu$, and we apply the equation, we'd be effectively undoing the batch normalization.[^1]

Then, when computing the gradients, we'd use $Z_{lnorm}$ instead of the unnormalized $Z_l$.

When using BatchNorm in a neural network, it effectively cancels out the effect of a bias term, making the inclusion of the computation of the bias computationally inefficient.

So when you use Batch normalization, you can effectively remove $b^l$ or set it to 0.

---

- [ ] Andrew Ng
- [ ] Sebastian Raschka
- [ ] Understanidng Deep LEarning
- [ ] Deep learning book
- [ ] Paper
- [ ] Implementation
	- [ ] Regular BatchNorm
	- [ ] BatchNorm in Adam + AdaMax

[^1]: And essentially, we'd be computing an identity function 