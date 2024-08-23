Say we have $n$ datapoints where $n$ is an arbitrary high dimension, $x_i \in {x_1, x_2, ..., x_n}$

Given $x_i$, what is the probability that $x_j$ is its neighbor?

An easy way to do this is to use an algorithm, $\mathbb{A}$, similar to a [[K-Nearest-Neighbors Classifier]] with $K = 1$, by computing a function, $g(x_i)$, to determine the shortest distance between the given $x_i$ and all possible $x_j$, given by $||x_i - x_j||^2$ ([[euclidean distance]]) to return the $1st$ nearest neighbor as the nearest neighbor.

$P_{j|i} = g(x_i)$

where $P_{j|i}$ is the probability that $x_j$ is the nearest neighbor to a given $x_i$.

The issue with this is that as dimensions, $n$, continues to increase, computing neighbors as the nearest euclidean distance becomes unreliable as each datapoint $x_j$ essentially becomes near equidistant to each other[^1]

Instead, you can compute a function that uses the nearest distance between $x_i$ and $x_j$, $d_{ij} = g(x_i)$ and the distances of the given $x_i$ to all other possible values, $x_{k≠j}$:

$P_{j|i} = f(d_{ij}, d_{ik})$

where $P_{j|i}$ is the probability that $x_j$ is the nearest neighbor to a given $x_i$.

This function, $f$, can be defined as 

[^1]: [[Curse of Dimensionality]]