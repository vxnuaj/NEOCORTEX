Say we have $n$ datapoints where $n$ is an arbitrary high dimension, $x_i \in {x_1, x_2, ..., x_n}$

Given $x_i$, what is the probability that $x_j$ is its neighbor?

An easy way to do this is to use an algorithm, $\mathbb{A}$, similar to a [[K-Nearest-Neighbors Classifier]] with $K = 1$, by computing a function, $f(x_i)$, to determine the distance between the given $x_i$ and all $x_j$ to return the $1st$ nearest neighbor as the nearest neighbor.