> [Original Paper](https://arxiv.org/pdf/1502.03167)

**Abstract**

- Deep Neural Networks are complicated by the fact that the distribution of each layer's inputs changes, thereby changing the parameters of the model adjacently. 
- This can make a model take longer to learn as it has to iteratively adjust the distribution of the parameters in terms to the distribution of the inputs per layer, thereby also complicating the surface of the loss function.
- This is called Internal [[Covariate Shift]].
- The solution is to make normalization a part of a model's architecture per ***layer*** with a different normalization factor ( in terms of $var$ and $\mu$ ) per each mini-batch.
- This then allows for a model to use higher learning rates, care less about weight initialization, and improve training speeds.

**Introduction**

- [[Gradient Descent]] / [[Stochastic Gradient Descent]] has been key to deep learning.
- But it requires careful tuning of model [[Hyperparameters]], especially the learning rate and the means of [[Weight Initialization]]. 
- Training a model then also turns out to be complicated by the fact that per each input to each layer, the distribution of inputs iteratively changes per layer during training given the continuous adjustments of model weights and biases. This is called [[Covariate Shift]]
- Therefore, a model has to change the distribution of it's weights constantly to represent the dataset, making it difficult for it to converge on the optima of the loss, faster.
- Considering a network with the $sigmoid$ activation, $\frac{1}{1 + exp(-x)}$, for very high or low values of $x$, you can encounter a vanishing gradient problem which becomes worse in the deeper a network gets.
- You can address it with the $ReLU(x)$ activation and careful weight initiaization ([[He Initialization]] & [[Xavier Initialization]]), and small values of $\alpha$, but it'd be more effective to center the distribution of inputs to the activation functions around a fixed size to avoid this [[vanishing gradient]].

- Then, normalizing these distributions mitigate the [[covariate shift]], [[vanishing gradient]]s, and increase training times + learning rates ($\alpha$).
- It allows for a model to use activation functions that are prone to saturation ([[sigmoid]], [[Tanh]]) without getting stuck in the saturating regions (meaning extremely large or small values).

**Towards Reducing Internal Covariate Shift**

- It's been known that whitening ($\mu := 0$, $var := 1$) the inputs of a model can increase training speed (by decorrelating the activations to their inputs, given the normalization)
- The same can be done for each layer, to remove the effects of [[Covariate Shift]].
- Considering a model, say $f$, that's composed of inputs $u$, a bias $b$, and a shift in the mean by $x$, to get an output $\hat{x}$. Shifting the affine transformation by $b$, and then subtracting the mean, $x$, would lead to a cancelling effect where $b$ eliminates the effect of subtracting the mean, $x$.
- Then the gradient of the loss function with respect to $b$ will not change in value whilst undergoing the update step, $b = b - \alpha \cdot \frac{∂L}{∂b}$, while the paramter $b$ will still iteratively update thereby causing an exploding or vanishing of the parameter $b$ in terms of it's value.
- So to mitigate this, again, introducing a narrowed distribution for the inputs to each layer would be ideal as it would allow for the gradient of the loss with respect to model parameters to account for the normalized distributions and scales.
- This can be done through [[Z-Score Normalization]], where it is:

	$\hat{x} = \frac{x - E[x]}{\sqrt{Var[x]}}$

- Though, then normalizing the input of a layer might change what the original layer can represent and in the case of using [[sigmoid]], $\frac{1}{1 - e^{-x}}$, might make inputs $\hat{x}$ remain centered in the linear zone of the [[sigmoid]]. 
- So to mitigate this, you can introduce a 