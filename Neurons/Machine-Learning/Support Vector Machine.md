A linear support vector machine is a linear classifier that aims to draw a boundary between a set of datapoints, based on a linear decision boundary and "[[Support Vectors]]".

The decision boundary is defined as $w \cdot x + b = 0$.

The weights $w$, represent the hyperplane or decision boundary that separates the classes in $x$ as best as possible. They yield the coordinates of a vector orthogonal to the hyper plane.

Therefore the $L_2$ norm of $w$, as $||w||$, will yield the distance between the decision boundary and it's corresponding [[Support Vectors]].


The weight vector of $w$, represents the maximum distance between the given classes $x$. Note that $w$ is orthogonal to $x$, thereby the decision boundary is ultimately defined by $b$.[^1]


---


The goal of a support vector machine is to find the decision boundary that best separates the classes. We want to find the [[Support Vectors]] which correspond to the largest gap between the decision boundary and the datapoints.

To classify predictions, if the SVM bases it's binary classifications based on the sign of an output. 

If the prediction of an SVM $f(x)$ is $>0$, the prediction class is $+1$, while if $f(x) < 0$, the prediction class is $-1$.

Unlike other classifiers, the support vector machine relies on the [[Hinge Loss]] as it's loss function.

A support vector machine can be sensitive to outliers, where if a single datapoint of a different class is grouped near to datapoints of different classes, then the decision boundary and [[support vectors]] will skew, indicating a level of overfitting.

Thereby, we can rely on [[Regularization for SVMs]], similar to [[L2 Regularization]] where we add an additional loss penalty to the [[hinge loss]].

[^1]: True? or Not?