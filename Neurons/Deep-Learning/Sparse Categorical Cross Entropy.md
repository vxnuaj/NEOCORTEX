Sparse categorical cross entropy, another [[Loss function]] that is similar to [[categorical cross entropy]], is designed for multiclass classification problems where labels are "sparse" meaning that each sample can only belong to one class and other classes become irrelevant.

The key difference from [[categorical cross entropy]] is the absence of [[one hot encoding]] the target labels for the calculation of the loss.

This sparse version of [[categorical cross entropy]] is used when the target labels of a dataset are represented in integers, representing the class index directly.
