#stats

Information Gain is a metric that denotes the amount of useful information that a given feature yields, to reduce the uncertainty or information entropy in a given scenario.

It can be computed as:

$IG(D, A) = H(D) - H(D, A)$, where $D$ is a dataset and $A$ is a specific feature.

- $H(D)$ is the [[entropy]] of a given set of samples as, $- \sum_{i = 1}^K p_i log(p_i)$

- $H(D, A)$ is the [[weighted entropy]] of the subsets of the original $D$ as $\sum_{j=1}^n\frac{D_j}{|D|}H(D_j)$ where $n$ is the number of total subsets and $D_j$ is the number of total instances in the given subset. $H(D_j)$ is then the entropy of the given $D_j$. 

The subtraction, then yields the ***information gain***, which then denotes how much each additional feature or in the context of [[decision tree]]s, how much each node contributed to reducing the amount of disorder or uncertainty in the given problem.

The information gain, at a given split of a tree, serves as an indicator to which feature can be the most important to consider at a given split. When splitting the root node, the first split is done on the most important feature to split upon, denoted by the highest information gain.