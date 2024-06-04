> [LINK](https://jmlr.org/papers/volume15/srivastava14a/srivastava14a.pdf)

Introduction:

- Combining models to improve performance nearly always improves performance given that they were as trained on different samples of a dataset with a varied architecture[^1]
- Doing so with large neural networks and taking the average of the outputs[^2] can be computationally expensive.
- It's also daunting task to train multiple architectures and find the optimal hyperparameters as well as collect a good size of training data.

- Dropout aims to address the issues, by preventing overfitting and combining variations of neural network architectures in a more efficient manner.
- Dropout removes a set of neurons and keeps a set based on a keep probability $p$ where the probability of dropping a neuron is $1-p$

	![[Screenshot 2024-06-04 at 9.31.24 AM.png]]

- The result of applying dropout is then a thinner neural network, comprised of neurons *"that survived dropout"*
- There are a collection of $2^n$ thinned networks 

[^1]: Ensemble Models?
[^2]: Outputs are averaged in order to get the 'average prediction' of both models.