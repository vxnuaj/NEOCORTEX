Sparse categorical cross entropy, another [[Loss function]] that is similar to [[categorical cross entropy]], is designed for multiclass classification problems where labels are "sparse" meaning that each sample can only belong to one class and other classes become irrelevant.

The key difference from [[categorical cross entropy]] is the absence of [[one hot encoding]] the target labels for the calculation of the loss.

This sparse version of [[categorical cross entropy]] is used when the target labels of a dataset are represented in integers, representing the class index directly instead of [[One hot encoding]]s. 

It might be more beneficial to use this loss function when dealing with a large number of classes to avoid high memory use and increase computational efficiency.

But there are some detriments.

A loss of information can be present as you lose information from the overall dataset when you don't implement [[one hot encoding]]s. A model can't map relationships between classes as easily, as it will only know the index of the correct class. 