Beginning at minute 42ish.

> https://www.youtube.com/watch?v=lDwow4aOrtg&t=3322s

### Functional Margin

If given a model of [[logistic regression]], the task is to predict $1$ if the true label $Y$ is $1$. 

Thereby, if we're given an input $X$, with a true class label of $1$, we hope that the output prediction $\hat{Y}$ is $>> .5$, not merely $> .5$.

This is as we want the model to ideally be as confident as possible, not at the edge of choosing $0$ over $1$.

### Geometric Margin

Given a dataset of binary classes, that have wide gap with between datapoints between different classes and that are separable by a linear decision boundary, $A$, there can be an infinite number of variable $A$s that can separate the set of datapoints

What a [[Support Vector Machine]] does is find the optimal line or decision boundary that separates datapoints between each class.

The margin between the optimal line or decision boundary and a given datapoint is called the geometric margin, defined as:

