Random forests are a set of bagged decision trees, with the addition of some extra randomness to each tree.

Rather than only using [[Bootstrapped Samples]], a random forest has it's individual bagged decision trees trained on a random subset of features.

If we have $n$ total features, we choose $k$ features randomly at each node, where $k < n$, limiting a [[decision tree]] to choose the optimal feature split index from only the subset $k$.

Then per usual, you'd choose the split with the highest [[Information Gain]] through the [[Gini Index]] or [[Entropy]], to make the next split.

A typical choice of $k$ is $k = \sqrt{n}$

This is done to decorrelate each tree within the ensemble, to further reduce the variance and mitigate overfitting. 

> *Otherwise, an individual tree in the ensemble might still come up with similar splits to others.*

If each tree was overfit, given that [[Bootstrapped Samples]] still contain some similar data, the overall result may still yield an overfit prediction with high variance. 

Random Forests, decorrelating each tree through [[Bootstrapped Samples]] and a random selection of features, are able to produce results that are more generalizable.

The hyperparameters we can select are 

- The number of bootstrapped samples
- The number of Random Features to consider at each node.