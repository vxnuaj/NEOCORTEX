You can typically normalize the inputs to a neural network by applying [[Z-Score Normalization]] or another means of a simply division by $255$ for pixel values.

This works well for input features.

But, in deeper networks, you might also want to normalize the input features into each layer.

This is what [[Batch Normalization]] does.

We can normalize the linear transformation $(z_{l}$) to a scale that's more easily computable by a deep neural network.

> *Typically, its seems that batch normalization is applied prior to the activation function, after the linear transformation, though doing after the activation can work as well.* 




---

- [ ] Andrew Ng
- [ ] Sebastian Raschka
- [ ] Understanidng Deep LEarning
- [ ] Deep learning book
- [ ] Paper
- [ ] Implementation