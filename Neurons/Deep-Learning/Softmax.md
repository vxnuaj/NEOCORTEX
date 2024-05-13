#mathematics 

Softmax is an [[activation function]], commonly used in the output layer of neural networks build for multi-class classification.

It can be mathematically defined as:

$softmax(z) = \frac{e^z}{\sum e^z}$

which in code can be defined as:

```
softmax(z) = np.exp(z) / np.sum(np.exp(z), axis = 0, keepdims = True)

#Assuming that axis 0 is the number of classes. Otherwise, axis = 1.

```

It's derivative can be defined as:




---

- [ ] Mathematical Definition
- [ ] Code Definition
- [ ] Range
- [ ] Derivative
- [ ] Smoothness, is it smooth everywhere?
- [ ] Monotonicity
- [ ] Computational Efficiency
- [ ] Common Use Cases
- [ ] Advantages / Disadvantages
- [ ] Implementation in a Model vs Others