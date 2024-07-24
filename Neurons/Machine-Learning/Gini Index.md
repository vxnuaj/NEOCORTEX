#mathematics 

Used to quantify the impurity or disorder of a set of elements, particularly in decision trees.

It is defined as:

$G = \sum_{i = 1}^K p_i(1 - p_i)$

which can be simplified to:

$G = 1 - \sum_{i = 1}^K p_i^2$

where it's interval is in the range $[0, .5]$ and $p_i$ is the probability of an item being classified into class $i$

while for binary classification, it is defined as:

$G = p_1 ( 1 - p_1) + p_2(1-p_2)$

Say for binary classification, when a [[Decision Tree]] reaches it's leaf node, outputting a probability of $1$ for a choice, the Gini Index will be $0$ as:

$G = 0( 1 - 0) + 1(1-1) = 0$

Inversely, when the probability is $.5$ for the given choices, the Gini index will be $.5$ as:

$G = .5( 1 - .5) + .5(1-.5) = .25 + . 25$

When the Gini Index reaches $0$, a [[decision tree]] is essentially reached the leaf node and is sure of the decision it'd make based on the training data.