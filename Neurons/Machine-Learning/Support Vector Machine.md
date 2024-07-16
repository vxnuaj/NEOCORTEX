A support vector machine is a linear classifier that aims to draw a boundary between a set of datapoints, based on a linear boundary and "[[Support Vectors]]".

The goal of a support vector machine is to find the decision boundary that best separates the classes. We want to find the [[Support Vectors]] which correspond to the largest gap between the decision boundary and the datapoints.

To classify predictions, if the SVM bases it's binary classifications based on the sign of an output. 

If the prediction of an SVM $f(x)$ is $>0$, the prediction class is $+1$, while if $f(x) < 0$, the prediction class is $-1$.


Unlike other classifiers, the support vector machine relies on the [[Hinge Loss]] as it's loss function.