The KD-Tree is an alternative algorithm for a KNN, where prior to predicting the $kth$ nearest neighbors of a datapoint $X$, we split a set of datapoints by taking the median of a single feature across samples.

The data is split or segmented across samples until we hit a pre-defined parameter, which denotes the minimum number of samples for a node.

Then, we compute the [[K-Nearest-Neighbors Classifier]], as is, with the limits being that the $kth$ neighbor can only be computed for the specific segment that a sample is within.

