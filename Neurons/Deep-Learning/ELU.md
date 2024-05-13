The Exponential Linear Unit, or ELU, is an activation function similar to [[ReLU]] or [[Leaky ReLU]] with the exception that the lower bound of the function, curves into a flatter gradient rather than abruptly changing into one.

Mathematically, ELU can be defined as:

$ELU(z) = \begin{cases} z, z > 0 \\ \alpha(e^z -1 ), z <= 0 \end{cases}$

$ELU(z) = max(z, (alpha * (np.exp(z) - 1))$

while in code, this can be defined as:

```
alpha = .01

#ELU | Either works

elu = np.maximum(z, (alpha * (np.exp(z) - 1)))
elu2 = np.where(z > 0, z, (alpha * (np.exp(z) - 1)))
```

It's derivative can be defined as:

$ELU(z) = \begin{cases}1, z>0 \\ \alpha e^z, z <= 0\end{cases}$

while in code can be expressed as:

```
elu_grad1 = np.where(z > 0, 1, (alpha * np.exp(z)))
```

The range of ELU goes from $-\infty$ to $

---

- [x] Mathematical Definition
- [x] Code Definition
- [ ] Range
- [x] Derivative
- [ ] Smoothness, is it smooth everywhere?
- [ ] Monotonicity
- [ ] Computational Efficiency
- [ ] Common Use Cases
- [ ] Advantages / Disadvantages
- [ ] Implementation in a Model vs Others