Given a dataset of binary classes, that have wide gap with between datapoints between different classes and that are separable by a linear decision boundary, $A$, there can be an infinite number of variable $A$s that can separate the set of datapoints

What a [[Support Vector Machine]] does is find the optimal line or decision boundary that separates datapoints between each class.

The margin between the optimal line or decision boundary and a given datapoint is called the geometric margin, computed as the [[Euclidean Distance]] defined as:

$\gamma = \frac{y_i(w^Tx_i + b)}{||w||}$

where the numerator represents the predicted vector derived from the boundary $w$, inputs $x$, and bias $b$.

The denominator scales the input down based on the euclidean norm of $w$ or the distance from the decision boundary to the [[Support Vectors]]. This makes sure that when computing the geometric mean, the input $x$ is independent to scaling by $w$.