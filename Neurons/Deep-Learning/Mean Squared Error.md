The mean squared error is a [[loss function]], used to evaluate the error in a model. It does so by calculating the average squared difference between the observed and predicted values.

When used in [[linear regression]], MSE is the average squared residual of the model.

Mathematically, the MSE can be defined as:

$MSE = \frac{1}{m} \sum{(Y - \hat{Y})^2}$, $m = num_samples$

In code, this can be defined as

```
MSE = np.sum((y_train - y_pred)**2) * (1 / samples)
```

It's derivative, with respect to predicted values, $\hat{Y}$ can be defined as:

$\frac{∂MSE}{∂\hat{Y}} = -2(Y - \hat{Y})$

In code, this can be defined as:

```

```

**Advantages**
- Can be derived and easily used in [[Gradient Descent]]

**Disadvantages**
- Not robust to outliers. Given that it takes the squared difference, The MSE becomes extremely sensitive to outliers.

---

- [x] Definition, Mathematical and Code
- [ ] Derivative, Mathematical and Code
- [ ] Usage in regression, Concept and Implementation
- [ ] Characteristics