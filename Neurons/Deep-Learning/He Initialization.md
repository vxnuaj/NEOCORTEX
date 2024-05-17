He initialization serves a similar purpose as [[Xavier Initialization]] initialization that deals with the issue of an activation function not being centered around $0$ which is the case with [[ReLU]].

Mathematically, it can be defined as:

$W^{(l)} = W^{(l)} \cdot \sqrt{\frac{2}{m^{(l-1)}}}$, where $m$ is the number of input features to the current layer.

In code, it can be defined as:

```
w = np.random.randn(dim1, dim2) * np.sqrt(2/m)
```

This aims to preserve the variance of the gradients during [[Backward propagation]] to avoid anishing or exploding gradients, for the [[ReLU]] activation.


---
- [ ] Justify this, mathematically, how it aims to preserve variance once you learn the foundational math