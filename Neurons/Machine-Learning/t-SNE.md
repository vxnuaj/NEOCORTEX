Say we have $n$ datapoints where $n$ is an arbitrary high dimension, $x_i \in {x_1, x_2, ..., x_n}$

Given $x_i$, what is the probability that $x_j$ is its neighbor?

An easy way to do this is to use an algorithm, $\mathbb{A}$, similar to a [[K-Nearest-Neighbors Classifier]] with $K = 1$, by computing a function, $g(x_i)$, to determine the shortest distance between the given $x_i$ and all possible $x_j$, given by $||x_i - x_j||^2$ ([[euclidean distance]]) to return the $1st$ nearest neighbor as the nearest neighbor.

$P_{j|i} = g(x_i)$

where $P_{j|i}$ is the probability that $x_j$ is the nearest neighbor to a given $x_i$.

The issue with this is that as dimensions, $n$, continues to increase, computing neighbors as the nearest euclidean distance becomes unreliable as each datapoint $x_j$ essentially becomes near equidistant to each other[^1]

Instead, you can compute a function that uses the nearest distance between $x_i$ and $x_j$, $d_{ij} = g(x_i)$ and the distances of the given $x_i$ to all other possible values, $x_{k≠j}$:

$P_{j|i} = f(d_{ij}, d_{ik})$

where $P_{j|i}$ is the probability that $x_j$ is the nearest neighbor to a given $x_i$.

This function, $f$, can be defined as:

$P_{j|i} = \frac{e^\frac{-||x_i-x_j||}{2\sigma^2}}{\sum_{k≠i} e^{-\frac{||x_i - x_k||}{2\sigma^2}}}$

where the numerator and the term being $\sum$med in the denominator is the [[Radial Basis Function]], where the output of the RBF higher is there is a higher similarity between 2 datapoints, in this case $x_i$ and $x_j$ and the inverse of there is a lower similarity.

In this case, you can then see this function as a probability measure of a given $x_i$ and $x_j$ being neighbors compared with all other possible datapoints, $x_k$

Now using that function, to compute the probability of drawing $x_i$ and $x_j$ if we pick a point at random, we can do so as:

$P_{ij} = \frac{P_{j|i} + P_{i|j}}{2N} = \frac{P_{j|i}}{N}+\frac{P_{i|j}}{N}$

where $P_{ij}$ is the probability, serving as a similarity measure between $x_{i}$ and $x_j$ and $N$ is the number of datapoints in $X$.

We use both probabilities, $P_{j|i}$ and $P_{i|j}$ to symmetrically consider the probability as a hole. Given that $x_i$ and $x_j$ are different datapoints in an $\mathbb{R}^n$ vector space, their position would account for different probabilities.

We want to get both of their probabilities, to then compute a more overarching view of the similarity measure, $P_{ij}$

[^1]: [[Curse of Dimensionality]]