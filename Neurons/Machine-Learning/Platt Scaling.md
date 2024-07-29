Platt scaling is a means to convert the raw scores of a classifier into probabilities via the addition of a [[logistic regression]] model.

Say we have a [[Support Vector Machine]] and we want to output probabilities.

The [[logistic regression]] is trained on the raw outputs of the [[Support Vector Machine]] with respect to a set of true labels of the training set.

As $\frac{1}{1 + e^{Af(x) + B}}$, where $A$ and $B$ are parameters to the raw outputs of the [[Support Vector Machine]].

To avoid overfitting, platt scaling is typically applied to a subset of the training set, analogous to a calibration or dev set, which is held out to be unseen by the original [[Support Vector Machine]]

TLDR (notes to self):

- Fully train the [[Support Vector Machine]]
- You train the logistic regression model on the raw outputs of the [[Support Vector Machine]] with respect to labels of a calibration set, not the original dataset.
- This model is used to then map the outputs of the [[Support Vector Machine]] to probabilities during testing