#mathematics 

Softmax is an [[activation function]], commonly used in the output layer of neural networks build for multi-class classification.

It can be mathematically defined as:

$softmax(z) = \frac{e^z}{\sum e^z}$

which in code can be defined as:

```
softmax(z) = np.exp(z) / np.sum(np.exp(z), axis = 0, keepdims = True)

#Assuming that axis 0 is the number of classes. Otherwise, axis = 1.

```

The range of softmax is from $0$ to $1$, outputting a probability of an input belonging to a specific class. 

It being bounded makes it suitable for the computation of a probability, as it also divides the exponential, $e$, raised to given class $z$, over the sum of $e$ raised to all classes $z$. The function requires the output of all classes to be equal to $1$, reinforcing it's use for computing a probability.

Softmax is smooth everywhere, mathematically unlike [[ReLU]] and it's variants. This allows for backpropagation to work effectively throughout the entire network ultimately mitigating the propagation of NaN values throughout a model.

It's continuity allows for gradient descent to slowly update parameters in a continuous fashion with no abrupt changes. Being monotonically increasing then allows for easier interpretability of the learning behavior of a model.

Softmax is less computationally efficient than most activation functions such as [[ReLU]], [[sigmoid]], 
or [[tanh]], but it's primarily used in the output layers of a model making this not much of an issue.

Common use cases of softmax are primarily only multi-class classification problem, being used in the final output layer. Going more complex, it can be used in attention mechanisms to compute the attention weights.

**Difference Between Sigmoid:**

While both sigmoid and softmax yield outputs between 0 and 1, the ability of Softmax to $\sum e^z$, allows for the computation of a probability as it's divided with $e^z$. Sigmoid on the other hand is defined as $\frac{1}{1 + e^{-z}}$ which is only able to compute a probability over 2 classes, $0$ or $1$.

**Advantages:**
- Ability to compute a probability of exponentials for a final output
- Interpretable outputs

**Disadvantages:**
- Can be computationally expensive
- Gradients near 0 can lead to a vanishing gradient problem for earlier layers in deep networks
- Ineffective with sparsity, given that we always need compute exponentials of all classes even if some inputs are $0$.