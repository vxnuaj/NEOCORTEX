The Mean Absolute Error is a [[loss function]], similar to the [[Mean Squared Error]], but rather computing the absolute difference rather than the squared difference.

Mathematically, it's defined as:

$MAE = \frac{1}{m}\sum | - \hat{Y}|, m = numsamples$

While in code, this can be defined as

```
MAE = (1 / samples) * np.sum(np.abs(y_train - y_pred))
```

It's derivative can be defined as:

$sgn(Y - \hat{Y})$

>*[[sgn(x)]]*

While in code this can be defined as:

```
MAE_deriv = (1 / samples) * np.sum(np.sign(y_train - y_pred))
```

Just as the [[Mean Squared Error]], MAE is used in [[linear regression]] as a validation metric. It's output value is the average difference between a true value and a prediction.

Think of it as the average absolute [[residual]] of a model.

MAE is robust to outliers, giving that it computes the error on the real diffe

---
- [x] Definition, Mathematical and Code
- [x] Derivative, Mathematical and Code
- [ ] Usage in regression, Concept and Implementation
- [ ] Characteristics`