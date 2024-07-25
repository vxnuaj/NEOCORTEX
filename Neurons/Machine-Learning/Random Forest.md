Random forests are a set of bagged decision trees, with the addition of some extra randomness to each tree.

Rather than only using [[Bootstrap Samples]], a random forest has it's individual bagged decision trees trained on a subset of random features.

This is done to decelerate each tree within the ensemble, to further reduce the variance and mitigate overfitting. 

If each tree was overfit, given that [[Bootstrap Samples]] still contain some similar data, the overall result may still yield an overfit prediction with high variance. 

Random Forests, decorrelating each tree through [[Bootstrap Samples]] and a random selection of features, are able to produce results that are more generalizable.