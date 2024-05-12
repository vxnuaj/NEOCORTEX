#mathematics 

Activation Functions are a type of function utilized in neural networks that aim to introduce non-linearity to a set of outputs, typically the [[weighted sum]]. 

The non-linearity introduced then allows for a neural network to capture more complex relationships and patterns from a given input.

Each activation function has a set of key features, that need to be considered when implementing a neural network:

1. Non-linearity

	The introduction of nonlinearity proves to be extremely important for a neural network as it allows for it to capture complex features and datapoints from a set of inputs. Without activation functions, a neural network would essentially be a set of linear combinations, unable to produce quality results to solve complex problems.

2. Range

	Activation functions have different ranges, some ranging from $0$ to $1$, others from $0$ to $infinity$, and others from $-1$ to $1$. 
	
	The output range of an activation function can be important to consider, for a variety of factors. 
	
	It's range can affect the scale of gradients during [[backward propagation]] leading to exploding or vanishing gradients, the numerical stability, and the interpretability of an activation function (some, such as [[softmax]], can be seen as a probability).

3. Monotonicity

	[[Monotonicity]], ensures that as the input of a model changes, the output remains consistently moving in a given direction (increasing or decreasing). 
	
	This can be important for the interpretability of a model (especially when computing probabilities), the gradient descent

5. Continuity
6. Differentiability
7. Sparsity
8. Computational Complexity