Categorical Cross Entropy Loss, similar to [[Binary Cross Entropy Loss]], is loss function that's used in multi-class classification in order to estimate the probability of a given input belonging to a specific class.

>*Also known as the [[Softmax]] Loss*

CCE comes into play when we begin to compute the probability of multiple classes. 

We could instead just consider such a problem as multinomial logistic regression, each class having a probability computed for a singular class separately but being inefficient to compute, as well there being the chance that the computed probabilities for each class end up greater than 1, we can use CCE alongside the [[Softmax]] function.

This essentially combines the multinomial logistic regression into a singular model.

- [ ] Definition, Mathematical and Code
- [ ] Derivative, Mathematical and Code
- [ ] Usage in regression, Concept and Implementation
- [ ] Characteristics