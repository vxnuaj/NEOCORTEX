Nadam, merges the [[Adam]] optimizer and the [[Nesterov Momentum]], by replacing the original computation of [[Momentum]] with [[Nesterov Momentum]].

This then allows for [[Adam]] to leverage the benefits that [[Nesterov Momentum]] may have in finding a more precise gradient while still making use of the second moment term ([[RMSprop]])

**So, mathematically, this can be defined as:**

$\theta_{lookahead} = \theta - \beta *  v\theta_{t-1}$
$a1, a2, z1, z2 = forward()$
$∂J(\theta_{lookahead}) = backward(a1, a2, z1, z2)$
$v\theta_t = \beta * v\theta_{t-1} + ( 1 - \beta) * ∂J(\theta_{lookahead})$
