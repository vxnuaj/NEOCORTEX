Entropy is the measure of uncertainty or probabilistic disorder in a system, given probabilities $p_i$, where $i$ is a given class.[^1]

$Entropy = - \sum_{i = 1}^K p_i log(p_i)$

Given a 2 class problem where $K = 2$, it can be defined as:

$Entropy = - \sum_{i = 1}^K p_1 log(p_1) + (1 - p_2) log(1 - p_2)$

where $p_1$ is the probability of the 1st class and $p_2$ is the probability of the second class.

The bounds of entropy are $[0, 1]$.

[^1]: Similar to [[Binary Cross Entropy Loss]] or [[Categorical Cross Entropy Loss]] 