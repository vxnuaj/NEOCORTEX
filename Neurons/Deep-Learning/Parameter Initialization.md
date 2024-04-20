When initializing parameters, it's never a good idea to initialize the weights, $W$, to 0. You can initialize the bias, $B$ to 0, but never $W$.

Initializing all the weights in $W$ to $0$ will lead to every neuron in the network computing the same function. During each weight update[^1], after each iteration, the weights in $W$ will be equivalent to each other. 

Each weight in $W$ will end up learning the same features and will fail to learn any meaningful representations of a dataset.

It's always better to initialize $W$ to randomly assigned parameters, `np.random.rand()`

[^1]:   : $θ = θ - ⍺ * \frac{∂L}{∂θ}$, see [[update rule]]