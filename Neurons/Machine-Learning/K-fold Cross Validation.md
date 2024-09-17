In K-fold cross validation, the dataset is split into different $\mathcal{K}$ folds of training and testing sets, where each fold has a unique set of training and testing data, of same size across folds.

A unique model is trained across different folds and the loss and accuracy metrics are averaged to get a true error metric.

This can eliminate the risk of overfitting and gives a more broader view of what true model error is on a generalized dataset.

