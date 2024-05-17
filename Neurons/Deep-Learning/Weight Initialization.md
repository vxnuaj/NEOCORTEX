Weight Initialization is important to consider when training a model as it might define how well and fast a model trains over a period of time.

The goal of weight initialization is to initialize model weights to small random numbers to break symmetry in the parameters.

>_If there's symmetry in the weights, the model won't be able to learn meaningful representations of a dataset_

We want the parameters to be small, in order to avoid exploding gradients and improve speed of convergence during learning.

The means to do so can be dependent on the type of [[activation function]], model architecture, and other hyperparameters.

Common types include [[Xavier Initialization]], [[He Initialization]]



---
- [ ] If the weights are too small, don't we get a vanishing gradient problem? Why is this or isn't the case?