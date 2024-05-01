Xavier initialization is a method of initializing the weights in a neural network in a way that prevents the activation outputs from exploding or vanishing during the forward pass of a neural network.

The idea is to initialize the weights in a way that the variance of the outputs of each layer is equal to the variance of its inputs. 

In this way, exploding or vanishing gradients are avoided during the training process as well as exploding outputs where overflow becomes an issue.

Mathematically, weights are initialized as $\frac{1}{features}$[^1]

[^1]: Mathematically, what's the justification? Why does this work?