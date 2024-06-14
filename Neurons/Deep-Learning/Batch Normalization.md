In deeper networks, you might want to normalize the input features into each layer to mitigate [[Covariate Shift]] and allow for faster learning.

This is what [[Batch Normalization]] does.

We can normalize the linear transformation $(z_{l}$) to a scale that's more easily computable by a deep neural network.

> *Typically, its seems that batch normalization is applied prior to the activation function, after the linear transformation, though doing after the activation can work as well.* 

Batch Normalization can then be applied per layer to the weighted sum, $z_l$.

$\mu = \frac{1}{m} \sum_{i=1}^m Z_l^i$, where $m$ is the number of input neurons to the following layer.
	
$Z_l^i = Z_l^i - \mu$

$\sigma^2 = \frac{1}{m} \sum_{i = 1}^m (Z_l^i - \mu)^2$, where $m$ is the number of input neurons to the following layer.

$Z_{lnorm} = \frac{Z_l}{\sqrt{\sigma^2 + \epsilon}}$

This defines a batch normalization layer.

Afterward, the mean and variance of the $Z_{norm}$ can be adjusted through parameters $\gamma$ and $\beta$.

$\tilde{Z_{lnorm}^i} = \gamma Z_{lnorm}^i + \beta$

$\gamma$ is known as the scale parameter, which can be used to scale the normalized value It can either amplify or dampen the scale of $Z_{lorm}$ based on what's more beneficial for model performance

$\beta$ is the parameter to shift the distribution of the normalized values, to better fit the desired output distribution to optimize model performance.

The $\gamma$ and $\beta$ parameters should be matrices of same dimensions as output $Z^l$.

*These aren't [[Hyperparameters]], but instead learnable parameters during [[gradient descent]]*.

Of course if $\gamma = \sqrt{\sigma^2 + \epsilon}$ and $\beta = \mu$, and we apply the equation, we'd be effectively undoing the batch normalization.[^1]

Then, when computing the gradients, we'd use $Z_{lnorm}$ instead of the unnormalized $Z_l$.

When using BatchNorm in a neural network, it effectively cancels out the effect of a bias term, making the inclusion of the computation of the bias computationally inefficient.

So when you use Batch normalization, you can effectively remove $b^l$ or set it to 0.

During training, the $\gamma$ values are typically initialized to a matrix of $1$'s and the $\beta$ values are typically initialized to a matrix of $0$s, with dimensions equivalent to the weighted sum $Z$ and layer $l$.

Then during training, after the forward pass, during the backward pass you compute the gradient of the loss with respect to $\gamma$ and $\beta$ and apply the parameter update as you would for any other parameter $W$ or $B$ within your model, yet with a slightly different derivation in regards to the backpropagation.

The [[gradient descent]] for a 2 layer neural network with batch normalization is mathematically defined as:

> *We'll be using $ReLU$ and $Softmax$ as they are the most common in multi-class classification but they can be replaceable with any other activation function, given a slight change to the derivation of the gradients. 

--- start-multi-column: ExampleRegion1\
```column-settings
number of columns: 2
border: off
border-shadow:off
largest column: right
```
#### *Forward Pass*
$Z_1 = W_1 • X$
$Z_{1norm} = batchnorm(Z_1)$
$\tilde{Z_{1norm}}= \gamma_1 \cdot Z_{1norm} - \beta_1$
$A_1 = ReLU(\tilde{Z_{1norm}})$

$Z_2 = W_2 \cdot A_1$
$Z_{2norm} = batchnorm(Z_2)$
$\tilde{Z_{2norm}}= \gamma_2 \cdot Z_{2norm} - \beta_2$
$A_2 = Softmax(\tilde{Z_{2norm}})$

$Loss = CCE(A_2, Y_{onehot})$

---break-column---

#### *Backward Pass*

$\frac{∂L}{\tilde{∂Z_{2norm}}} = (\frac{∂L}{∂A_2})(\frac{∂A_2}{\tilde{∂Z_{2norm}}}) = A_2 - Y_{onehot}$
$\frac{∂L}{∂\gamma_2} = (\frac{∂L}{\tilde{∂Z_{2norm}}})(\frac{∂\tilde{Z_{2norm}}}{∂\gamma_2}) = \frac{∂L}{\tilde{∂Z_{2norm}}} * Z_{2norm}$
$\frac{∂L}{∂\beta_2} = (\frac{∂L}{\tilde{∂Z_{2norm}}})(\frac{\tilde{∂Z_{2norm}}}{∂\beta_2}) = \sum \frac{∂L}{\tilde{Z_{2norm}}}$, *summed over number of samples in the batch*
$\frac{∂L}{∂Z_2} = (\frac{∂L}{\tilde{∂Z_{2norm}}}) (\frac{\tilde{∂Z_{2norm}}}{∂Z_{2norm}})(\frac{∂Z_{2norm}}{∂Z_2}) = \frac{∂L}{\tilde{∂Z_{2norm}}} * \gamma_2 * \frac{1}{|{\sigma_2}|}$
$\frac{∂L}{∂W_2} = (\frac{∂L}{∂Z_2})(\frac{∂Z_2}{∂W_2}) = (\frac{∂L}{∂Z_2}) \cdot A_1^T$
$\frac{∂L}{\tilde{∂Z_{1norm}}} = (\frac{∂L}{∂Z_2})(\frac{∂Z_2}{A_1})(\frac{∂A_1}{∂Z_{1norm}}) = W_2^T \cdot \frac{∂L}{∂Z_2} * ReLU_{deriv}(\tilde{Z_{1norm}})$
$\frac{∂L}{\gamma_1} = (\frac{∂L}{\tilde{∂Z_{1norm}}})(\frac{\tilde{∂Z_{1norm}}}{∂\gamma_1}) = (\frac{∂L}{\tilde{Z_{1norm}}}) * Z_{1norm}$
$\frac{∂L}{∂\beta_1} = (\frac{∂L}{\tilde{∂Z_{1norm}}})(\frac{\tilde{∂Z_{1norm}}}{∂\beta_1})$
$\frac{∂L}{∂Z_1} = (\frac{∂L}{\tilde{∂Z_{1norm}}}) (\frac{\tilde{∂Z_{1norm}}}{∂Z_{1norm}})(\frac{∂Z_{1norm}}{∂Z_1}) = \frac{∂L}{\tilde{∂Z_{1norm}}} * \gamma_1 * \frac{1}{|{\sigma_1}|}$
$\frac{∂L}{∂W_1} = (\frac{∂L}{∂Z_{1}})(\frac{∂Z_1}{∂W_1}) = (\frac{∂L}{∂Z_1}) \cdot X^T$

---end-multi-column

**Why BatchNorm works**:

BatchNorm essentially allows for us to center the inputs fed into each activation function, allowing for the model to ultimately generalize on more data.

> *This is the case in RGB images, where a model is trained on identifying black cats. If you introduce BatchNorm and then input normalization during testing, the model would be able to identify the colored cats as well.
> 
> BatchNorm would help the model learn more robust features without being sensitive to color intensities, though of course, you'd have to normalize the input of colored cats during testing*

This helps mitigate what's called [[covariate shift]], or when the distribution of the data changes amongst layer of a model.

In essence, the inputs to each layer can be seen as features. But as parameters and activations from previous layers change, the distribution of the input features to later layers changes, introducing again [[covariate shift]]

This type of *[[covariate shift]]* makes a model learn slower as it continuously has to adjust it's parameters to an ever changing distribution of gradients, which gets worse as a neural network gets deeper.



This then also reduces the need for extensive amounts of data (*in our example, we'd only need data for black cats, while still generalizing to colored cats*)



---

- [ ] Andrew Ng
- [ ] Sebastian Raschka
- [ ] Understanidng Deep LEarning
- [ ] Deep learning book
- [ ] Paper
- [ ] - [ ] Implementations

[^1]: And essentially, we'd be computing an identity function 