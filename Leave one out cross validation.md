An extreme end to [[K-fold Cross Validation]], where one model is created for the number of samples in a dataset.

Here, a model is trained on all samples with one sample left out to be used for testing.

This is done over all samples, with a then averaged loss to get a more representative error.