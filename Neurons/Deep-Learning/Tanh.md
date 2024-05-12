Tanh is an [[activation function]] (known as the hyperbolic tangent), which is defined as:

$tanh = \frac{e^z - e^{-z}}{e^z + {e^{-z}}}$

and code defined as:

```
tanh = (np.exp(z) - np.exp(-z)) / (np.exp(z) + np.exp(-z))
```

It's derivative can be defined as:

$= \frac{(e^z + e^{-z})(e^z - e^{-z})' - (e^z - e^{-z})(e^z + e^{-z})'}{({e^z + e^{-z}})^2}$

$= \frac{(e^z + e^{-z})^2 - (e^z - e^{-z})^z}{(e^z + e^{-z})^2}$

$= \frac{(e^z + e^{-z})^2}{(e^z + e^{-z})^2} - \frac{(e^z - e^{-z})^2}{(e^z + e^{-z})^2}$

$= 1 - tanh(z)^2$ 

It's range is between, $-1$ and $1$ symmetric around the origin of $0,0$.

**Advantages**

1. The range between $-1$ and $1$ means that it has 


---

- [x] Mathematical Definition
- [ ] Range
- [x] Derivative
- [ ] Smoothness, is it smooth everywhere?
- [ ] Monotonicity
- [ ] Computational Efficiency
- [ ] Common Use Cases
- [ ] Advantages / Disadvantages



