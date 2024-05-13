Swish is an activation function proposed by a team of Google researchers in 2017.

Mathematically, it can be defined as:

$Swish(z) = z sigmoid(\beta z) = \frac{z}{1+e^{-\beta z}}$,

where $\beta$ is a tunable parameter. If set to $1$, $Swish$ is essentially a sigmoid multiplied by it's input.

In code, this can be defined as:

```
def swish(z, beta = 1)
	return z * (1/(1+np.exp(beta * -z)))
```

It's range is from 

- [ ] Mathematical Definition
- [ ] Range
- [ ] Smoothness, is it smooth everywhere?
- [ ] Monotonicity
- [ ] Computational Efficiency
- [ ] Common Use Cases
- [ ] Advantages / Disadvantages
- [ ] Implementation in a Model vs Others