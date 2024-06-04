Early stopping is a [[Regularization]] technique that prevents overfitting by iteratively checking the performance on a validation dataset and stopping training as the performance begins to decay.

While you want to optimize the cost function, you don't want your model to overfit and instead you want generalization (reducing variance)

The **downside** is that you're reaching a consensus amongst the cost function and not overfitting.

Instead you can try L2 regularization and train your model for longer.l2