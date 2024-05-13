Leaky ReLU is an activation function based on [[ReLU]] with e difference being that when $z < 0$, it has a small gradient rather than having a $0$ gradient.

Mathematically, it is defined as:

$LeakyReLU(z) = \begin{cases} z, z>0 \\ 0.01z, z<0 \end{cases}$

$LeakyReLU(z) = max(.01z, z)$

In code, this can be defined as:

```
leaky_relu = np.where(z > 0, z, (.01 * z))
```

The derivative of Leaky ReLU can be defined as:

$LeakyReLU'(z) = \begin{cases} 1, z > 0 \\ .01, z < 0 \end{cases}$

```
def leaky_relu_gradient(z):
	if z > 0:
		return 1
	elif z < 0:
		return .01
```


---

- [ ] Mathematical Definition
- [ ] Code Definition
- [ ] Range
- [ ] Derivative
- [ ] Smoothness, is it smooth everywhere?
- [ ] Monotonicity
- [ ] Computational Efficiency
- [ ] Common Use Cases
- [ ] Advantages / Disadvantages
- [ ] Implementation in a Model vs Others