Regularization is a technique that aims to mitigate variance and overfitting in a model by penalizing complexity.

It involves adding a small term to a loss function which penalizes for large weights.

$J(w,b) = \sum L(\hat{y}, y) + \lambda \cdot Penalty$

>*The penalty is typically the [[euclidean norm]] or the [[manhattan norm]]*

This trades a decrease in training accuracy for an increase in generalizability.

Common regularization techniques include [[L2 Regularization]] and [[L1 Regularization]]

---

- [ ] l1 reg
- [ ] manhattan norm
- [ ] l2 reg
- [ ] euclidean norm
- [ ] implementation of each in a model (check [this](https://www.youtube.com/watch?v=_SlPBbxuqas) out)

![[Screenshot 2024-05-21 at 10.13.56 AM.png]]
