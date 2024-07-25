#algebra

An expansion to binomials raised to an $nth$ power.

With this theorem, we can expand $(a + b)^n$ for any non-negative integer $n$, where $a$ and $b$ are any numbers.

$(a + b )^n = \sum_{k = 0}^n \begin{pmatrix}n \\ k \end{pmatrix} a^{n - k} b^k$

where:

- $\begin{pmatrix}n \\ k \end{pmatrix}$ is a [[Binomial Coefficient]]

> *The binomial theorem is able to compute the probability of observing $k$ successes in $n$ total trials, if $a$ is the probability of getting $k$ successes in $n$ trials while $(b)^{n-k}$ is the probability of getting $n-k$ failures.* 
>
> *Then, the output is the probability of failure.*