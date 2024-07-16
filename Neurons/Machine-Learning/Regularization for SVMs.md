Regularization in SVMs allows for the decision boundary and the corresponding [[support vectors]] to become non-complex, where the decision boundary doesn't overfit to nuanced features, and rather generalizes.

Similar to [[L2 Regularization]] or [[L1 Regularization]], we add a penalty term to the [[hinge loss]] of an SVM.

$L_{regularized} = SVMCost(\beta_i) + C ||\beta||$

where $C$ is the tunable hyperparameter denoting the level of regularization we want.

If $C$ is a large value, the regularization onto the model will be higher. 
If $C$ is a small value, the regularization onto the model will be smaller.

Note that if the [[hinge loss]] is smaller, the penalty term will be higher. Inversely, if the [[hinge loss]] is higher, the penalty term would be smaller.

This is as the smaller the [[hinge loss]] is, the more complex the coefficients $\beta_i$ are, thereby indicating that they might hold a higher value. 

Therefore, the calculation of the magnitude of $\beta_i$, as $||\beta||$, will be higher the lower the [[hinge loss]] is.