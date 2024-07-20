#stats

Information Gain is a metric that denotes the amount of useful information that a given feature yields, to reduce the uncertainty or information entropy in a given scenario.

It can be computed as:

$IG(D, A) = H(D) - H(D, A)$, where $D$ is a dataset and $A$ is a specific feature.

$H(D)$ is the [[entropy]] of a dataset as, $- \sum_{i = 1}^K p_i log(p_i)$.
$H(D, A)$ is the weighted entropy 