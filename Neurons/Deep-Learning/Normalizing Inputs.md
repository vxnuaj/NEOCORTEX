You typically want to normalize your inputs to improve model stability, decrease complexity of the problem, decrease biased weights, which can potentially increase accuracy and/or increase training speed. 

To visualize, the space of an non-normalized loss function looks like:
	
	![[Screenshot 2024-06-04 at 1.50.50 PM.png | 350]]

It's clear that the space of the function isn't uniform in variance and takes on a wider set of values. 

When doing [[Gradient Descent]], this can result in biased weights, where the parameters converge onto values of different scales.

This then leads to poorer performance during inference and increases complexity of a model thereby increasing computation time.


It's important to make sure you normalize your inputs the same way during training and testing.

Some methods of doing so are:

1. [[Z-Score Normalization]]