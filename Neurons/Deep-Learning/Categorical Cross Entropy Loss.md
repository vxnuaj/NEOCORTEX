Categorical Cross Entropy Loss, similar to [[Binary Cross Entropy Loss]], is loss function that's used in multi-class classification in order to estimate the probability of a given input belonging to a specific class.

>*Also known as the [[Softmax]] Loss*

Mathematically, this is defined as:

$CCE = -\sum Y(\log(\hat{Y}))$

While in code, this can be defined as:

```
CCE = - np.sum(y_train * np.log(y_pred))
```

It's derivative with respect to $z$, the weighted sum, can be defined as:

$CCE_{zderiv} = A - Y_{train}$

```
CCE_zderiv = a - y
```

CCE comes into play when we begin to compute the probability of multiple classes. 

We could instead just consider such a problem as multinomial logistic regression, each class having a probability computed for a singular class separately but being inefficient to compute, as well there being the chance that the computed probabilities for each class end up greater than 1, we can use CCE alongside the [[Softmax]] function.

This essentially combines the multinomial logistic regression into a singular model.

It's also non-linear allowing for the function to capture the non-linearities of a dataset effectively and learn from them.

It's fully differentiable, making it fit for the use of [[Gradient Descent]]

- [x] Definition, Mathematical and Code
- [x] Derivative, Mathematical and Code
- [ ] Usage, Concept and Implementation
- [ ] Characteristics