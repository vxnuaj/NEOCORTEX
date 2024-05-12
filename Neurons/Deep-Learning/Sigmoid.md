#mathematics 

The sigmoid function is an [[activation function]] commonly used in neural networks to introduce non-linearity, mathematically defined as:

$σ(z) = \frac{e^z}{e^z + 1}$

$σ(z) = \frac{1}{(e^z + 1)(e^{-z})}$

$σ(z) = \frac{1}{(e^z)(e^{-z})+e^{-z}}$

$σ(z) = \frac{1}{1 + e^{-z}}$

$σ(z) = \frac{1}{1 + e^{-z}}$

and in code, defined as

```

sigmoid = 1 / (1 + np.exp(-z))

```

The function is shaped as an S-shaped curve, in the range of $0 < \hat{y} < 1$, one of it's use cases being to compute an output as a probability of an input belonging to a given class.

It's most commonly used in the output layer binary classification models or [[logistic regression]].

It's derivative can be defined as:

$σ(z) = \frac{e^z}{e^z + 1}$

$σ(z) = (1+e^{-z})^{-1}$

$σ'(z) = - (1 +e^{-z})^{-2}(-e^{-z})$

$σ'(z) = - \frac{-e^{-z}}{(1 +e^{-z})^{2}}$

$σ'(z) = \frac{e^{-z}}{(1 +e^{-z})^{2}}$



