Regularization in SVMs allows for the decision boundary and the corresponding [[support vectors]] to become non-complex, where the decision boundary doesn't overfit to nuanced features, and rather generalizes.

This serves the use-case to create [[soft margins]], where if the data isn't linearly separable, these [[soft margins]] help to generalize to the non-linear dataset. 

This maximizes the accuracy rather than maximizing fit. A linear SVM won't be able to fit to a non-linear dataset, taking some error through regularization and [[soft margins]] turns out to be worth the trade off for better accuracy.

Similar to [[L2 Regularization]] or [[L1 Regularization]], we add a penalty term to the [[hinge loss]] of an SVM.

$L_{regularized} = SVMCost(\beta_i) + C ||\beta||$

where $C$ is the tunable hyperparameter denoting the level of regularization we want.

If $C$ is a large value, the regularization onto the model will be higher. 
If $C$ is a small value, the regularization onto the model will be smaller.

Note that if the [[hinge loss]] is smaller, the penalty term will be higher. Inversely, if the [[hinge loss]] is higher, the penalty term would be smaller.

This is as the smaller the [[hinge loss]] is, the more complex the coefficients $\beta_i$ are, thereby indicating that they might hold a higher value. 

Therefore, the calculation of the magnitude of $\beta_i$, as $||\beta||$, will be higher the lower the [[hinge loss]] is.

When this regularization term is introduced, the higher a parameter $C$ is, the greater the loss will be. 

Therefore, given that an extra penalty is introduced, the model weights are updated in a manner that allows for some error, by increasing the margin between the decision boundary and the [[support vectors]].