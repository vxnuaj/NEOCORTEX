Regularization is a technique that aims to mitigate variance and overfitting in a model by penalizing complexity.

It involves adding a small term to a loss function which penalizes for large weights.

$J(w,b) = \sum L(\hat{y}, y) + \lambda \cdot Penalty$

>*The penalty is typically the [[Euclidean Distance]] or the [[Manhattan Distance]]*

This trades a decrease in training accuracy for an increase in generalizability.

Common regularization techniques include [[L2 Regularization]] and [[L1 Regularization]]

---

- [x] l1 reg
- [x] manhattan norm
- [x] l2 reg
- [x] euclidean norm
- [ ] implementation of each in a model (check [this](https://www.youtube.com/watch?v=_SlPBbxuqas) out)

![[Screenshot 2024-05-21 at 10.13.56 AM.png]]
