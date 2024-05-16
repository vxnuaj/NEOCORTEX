Sparse Categorical Cross Entropy is a loss function, very similar to the [[Categorical Cross Entropy Loss]], with the difference in the form it takes in the encoded vector.

Rather than taking in a [[one hot encoding]] as an input, it takes in an integer encoding where each label is represented by a single integer, $1, 2, 3, ... K$, where $K$ is the total number of classes.

It's also mathematically defined differently than [[Categorical Cross Entropy Loss]], as:




- [ ] Definition, Mathematical and Code
- [ ] Derivative, Mathematical and Code
- [ ] Usage in regression, Concept and Implementation
- [ ] Characteristics