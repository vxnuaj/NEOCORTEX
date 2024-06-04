Regularization is a technique that aims to mitigate variance and overfitting in a model by penalizing complexity.

It involves adding a small term to a loss function which penalizes for large weights.

$J(w,b) = \sum L(\hat{y}, y) + \lambda \cdot Penalty$

>*The penalty is typically the [[Euclidean Norm]] squared or the [[Manhattan Distance]]*

This trades a decrease in training accuracy for an increase in generalizability.

In practice, implementing regularization on a bias term is omitted given it's low dimensionality and minimal impact when compared to the weights of a model.

Common regularization techniques include [[Dropout]], [[L2 Regularization]] and [[L1 Regularization]]

---

![[Screenshot 2024-05-21 at 10.13.56 AM.png]]
