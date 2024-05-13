ReLU is an [[activation function]] commonly used in the hidden layers of deeper neural networks, to introduce non-linearity.

Mathematically, it's defined as:

$ReLU(z) = \begin{cases} z, z>0 \\ 0, z<0 \end{cases}$

$ReLU(z) = max(0, z)$

In code, it can be defined as

```
ReLU = np.maximum(0, z)
```

It's derivative can be defined as:

$ReLU'(z) = \begin{cases} 1, z>0 \\ 0, z<0 \end{cases}$

In code, it can be defined as

```
ReLU_deriv = z > 0 

#Returns true or false, a boolean value. 
#This can typically be automatically converted into a 1 or 0 when used in an operation
```

![[Pasted image 20240513082059.png|450]]


The range of ReLU is from $0$ to $\infty$, providing a stable output of $0$ if the input $z$ is less than $0$ and a linear output of $z$ is the input $z$ is greater than $0$. 

Given that it isn't bound to a specific range such as [[sigmoid]] or [[tanh]], it's use case will not be for normalizing data and can be inefficient when calculating final outputs given a lack of interpretability. Like [[sigmoid]] can be used to calculate probabilities, ReLU can't be interpreted as such.

Given that it only outputs positive values which can be very large, it might not be suitable for certain use-cases. But it doesn't suffer from the vanishing gradient problem. Rather it's sparse when $z < 0$ and has a consistent output when $z > 0$.

ReLU is not a 'smooth' function throughout it's entire range. At $0$, ReLU is not differentiable, which can potentially cause problems, but it's unlikely that an input [[weighted sum]] will be completely 0 due to the linear combination and the addition of a bias parameter.

Either or, the lack of 'smoothness' can be bypassed in code through `z > 0`, where the discontinuity isn't factored in.

ReLU is a strictly monotonically increasing function. As the inputs increase, i


**Advantages**

**Disadvantages**
- ReLU can be prone to outputting dead neurons, where neurons always output zero. This happens when a neuron is always negative then causing it to never activate at a number other than $0$. (This can be mitigated using [[Leaky ReLU]] or [[Parametric ReLU]]).




---

- [x] Mathematical Definition
- [x] Code Definition
- [x] Range
- [x] Derivative
- [x] Smoothness, is it smooth everywhere?
- [ ] Monotonicity
- [ ] Computational Efficiency
- [ ] Common Use Cases
- [ ] Advantages / Disadvantages
- [ ] Implementation in a Model vs Others