The hinge loss is a [[loss function]] used for training classification models. 

It's made for maximum margin classifiers, meaning classifiers that aim to optimize the margin distance between classes. 

The hinge loss can be defined as:

$loss = max(0, 1 - y \cdot f(x))$

where $y$ is the true class label and $f(x)$ corresponds to a prediction from the given classifier, typically a [[Support Vector Machine]].

Thereby, if the classifier is uncertain about the classification where $f(x) = 0$, the $loss$ value will hit exactly $1$ as:

$max(0, 1 - y \cdot 0) \rightarrow max(0, 1 - 0) \rightarrow 1$

Note that the hinge loss does not punish correct classifications, 

- Does not punish correct classifications
- As soon as a datapoint enters the margins defined by the set of [[support vector]]s,  the loss value begins to rise.
- For the loss value corresponding to a decision boundary, the loss hits exactly 1, if the margin between .