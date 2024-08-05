Bagging, also known as bootstrap aggregating, is an [[Ensemble Learning]] method, that uses the same learning algorithm for all $n$ models within the Ensemble.

It uses $n$ [[Bootstrapped Samples]] to train $n$ total models.

Then, from each prediction from a given model, $f_i$, you can use the hard majority vote or the soft majority vote from [[Majority Voting Classifiers]] and [[Soft Voting Classifiers]] respectively, to compute the final prediction for the ensemble.

Given this, in Bagging, it is practical to overfit numerous models on different sets of [[Bootstrapped Samples]], and then take the $argmax$ of a set of averaged probabilities for a set of classes to get a more precise prediction.

> *Bagging is more geared for decision trees, so if you train multiple decision trees without pruning on different [[Bootstrapped Samples]], to overfit, and then take the hard or soft majority you'd hypothetically get a higher accuracy.*