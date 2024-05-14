The Binary Cross Entropy Loss is a loss function (BCE) which computes the error or loss of a model that computes a binary classification task.

BCE expects it's $Y$ labels to belong to binary classes of either $0$ or $1$ while it expects it's $\hat{Y}$ predicted labels to belong to a probability between $0$ and $1$.

Mathematically, it is defined as:

$BCE = -\frac{1}{m} \sum Y * \log(\hat{Y}) + ( 1 - Y) * \log(1 - \hat{Y})$, $m = numsamples$

which in code can be defined as:

```
m = num_samples

BCE = -(1/m) * np.sum(y_train * np.log(y_pred) + (1 - y_train) * np.log(1 - y_pred))
```



- [ ] Definition, Mathematical and Code
- [ ] Derivative, Mathematical and Code
- [ ] Usage in regression, Concept and Implementation
- [ ] Characteristics