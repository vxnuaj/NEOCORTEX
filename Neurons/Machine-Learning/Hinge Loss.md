The hinge loss is a [[loss function]] used for training classification models. 

It's made for maximum margin classifiers, meaning classifiers that aim to optimize the margin distance between classes. 

The hinge loss can be defined as:

$loss = max(0, 1 - y \cdot f(x))$

where $y$ is the true class label and $f(x)$ corresponds to a prediction from the given classifier, typically a [[Support Vector Machine]].

Thereby, if the classifier is uncertain about the classification where $f(x) = 0$, the $loss$ value will hit exactly $1$ as:

$max(0, 1 - y \cdot 0) \rightarrow max(0, 1 - 0) \rightarrow 1$

If a given label is $1$ and the predicted class is $2$, the $loss$ value will be:

$max(0, 1 - 1 \cdot 2) \rightarrow max(0, 1-2), \rightarrow 0$

Note that 
- The hinge loss does not punish correct classifications.
- The as soon as a datapoint enters the margins defined by the [[support vectors]] the loss value begins to rise.
- For the loss value corresponding to a decision boundary, the loss hits exactly 1.