Xavier Initialization is a form of [[Weight Initialization]], proposed by Xavier Glorot and Yoshua Bengio.

To initialize weights you,
1. Initialize weights from a Gaussian or uniform distribution
2. Scale the weights proportionally to the number of inputs to the layer.

Each layer, $l$, has initialized weights scaled based on the number of neurons / input features, at $l-1$, being input to the layer $l$.

This is defined as: $W^{(l)} = W^{(l)} \cdot \sqrt{\frac{1}{m^{(l-1)}}}$ where $m^{(l-1)}$ is the number of input features at the previous layer.

> _If the bias parameters aren't initialized to 0, implement the same scaling_

This type of initialization is typically used alongside the [[Tanh]] activation function. 

While [[Tanh]] is more robust against vanishing gradients when compared to [[Sigmoid]], it's still prone to vanishing gradients if the inputs are very large, positive or negative. 

Initializing model weights using Xavier Initialization helps improve on [[Tanh]] and mitigate the vanishing gradient problem.

Yet when introduced raw inputs of extremely high values, it can fail as the $\sqrt{\frac{1}{n_{in}}}$ might not be enough to reduce the weighted sum, $z$ as as viable input into $\sigma(x)$ or $tanh(x)$[^1]

---
- [ ] https://proceedings.mlr.press/v9/glorot10a/glorot10a.pdf
- [ ] Motivation / Purpose
- [ ] Formula / Mathematical Rationale
- [ ] Code Implementation
- [ ] Advantages / Disadvantages

[^1]: See 'instance 1', [here](https://github.com/vxnuaj/LABS/blob/main/DEEPLEARNING/NeuralNetworks/WeightInitialization/weightinit.ipynb) or weightinit.ipynb (locally)