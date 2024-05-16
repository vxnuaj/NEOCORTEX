Sparse Categorical Cross Entropy is a loss function, very similar to the [[Categorical Cross Entropy Loss]], with the difference in the form it takes in the encoded vector.

Rather than taking in a [[one hot encoding]] as an input, it takes in an integer encoding where each label is represented by a single integer, $1, 2, 3, ... K$, where $K$ is the total number of classes.

It's mathematically defined the same as [[Categorical Cross Entropy Loss]], with the exception of the type of input, $Y$. 

It's defined as:

$CE_{sparse} = - \frac{1}{m} \sum y_{intencoded} * \log{\hat{Y}}$






- [ ] Definition, Mathematical and Code
- [ ] Derivative, Mathematical and Code
- [x] Usage in classification, Concept and Implementation
- [ ] Characteristics