Similar to [[random forest]]s, but the subset of trees have more variance in their predictions, each tree is even more different than each.

While the [[Random Forest]] makes use of bootstrapping and random feature subsets at each node, Extremely Randomized Trees select a random feature **split** at each node, which increases the variability for each split, given that the **feature split** values vary per split randomly.

The hyperparameters we can change are the:

- The number of bootstrapped samples
- The number of Random Features to consider at each node.
- The number of Random Feature Splits (Threshold values) to consider