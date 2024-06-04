Dropout is a [[Regularization]] technique that eliminates / ignores a specific set of neurons to optimize the network size to reduce overfitting and improve generalizability.

It aims to reduce co-dependence / co-adaptation amongst neurons. Some neurons depend on others to do the 'hard work' while they sit by and not contribute to the overall output.

>*Dropout is more commonly used during training a model, and more commonly disabled during testing. Though, in research, some used dropout as a means of assessing the uncertainty in the predictions of a model to assess it's confidence and effectiveness.*

When you dropout neurons randomly, the 'lazy' neurons must start learning and begin to reduce reliance on the 'hard working' neurons.

In dropout regularization, dropping neurons out means making a set of neurons $0$, based on a probability $p$, and normalizing the rest of the neurons that aren't eliminated as $\frac{a}{1-p}$.

Mathematically, where the activation is $a$, dropout looks as:

$a' = \begin{cases} 0, \hspace{3mm} p \\ \frac{a}{1-p}, \hspace{3mm} otherwise \end{cases}$

where $a'$ is the 'dropped out' activations, $a$ are the original activations, and $p$ is the probability.

In code, this looks as:

```
# Assuming 'A1' is the activation matrix for a particular layer 
# and 'p' is the dropout probability (the probability of dropping out a neuron). 

# Initialize random dropout matrix 'D1' with the same dimensions as the activation matrix 'A1'. 

# Each entry in 'D1' is drawn from a uniform distribution over [0, 1). 

D1 = np.random.rand(A1.shape[0], A1.shape[1]) 

# Set entries in 'D1' to 0 where the value is less than the probability of keeping a neuron (1 - p), and to 1 where the value is greater than or equal to the probability of keeping a neuron. 

D1 = D1 < (1 - p) 

# Element-wise multiplication of the activation matrix 'A1' and the dropout mask 'D1' to apply dropout. Neurons corresponding to 0 in 'D1' are dropped out. 

A1 = np.multiply(A1, D1) 

# Scale the activations of the neurons that have not been dropped out by (1 - p) to maintain the expected value. 

A1 = A1 / (1 - p)
```

Then the resulting network is a subset of the entire network.

Each neuron should have an approximately similar scaled impact on the model before and after dropout. If the neurons that weren't dropped weren't normalized, the stability and performance of a network would diminish given that dropout reduces the scale of the neuron activations. 

![[Screenshot 2024-06-04 at 8.23.21 AM.png | 400]]


Another common way to implement dropout is [[Inverted dropout]].