Nesterov momentum is a variant of [[Momentum]], which serves a similar, yet upgraded means to compute the optima of the loss in a faster and more direct manner when compared to [[Momentum]].

You, in a sense, allow for the [[Gradient Descent]] to 'look ahead' and predict what the optimal next jump would be. This is done through a 'lookahead'.

This 'lookahead' is computed by **first**, computing the gradient at the current position using the previously accumulated gradient and making a big jump in the direction of the previously accumulated gradient.

This 'lookahead' term is more of a placeholder term, rather than serving as a real update of $\theta$

**2nd**, is then measuring the gradient at the location of where we ended up at after the big jump and then computing the accumulated gradient, to then finally compute the true update of $\theta$ using the newly accumulated gradient.

Then this process is repeated for all time steps / iterations.

This can be defined as:

$\theta_{lookahead} = \theta_t - \beta* v\theta_{t-1}$ 

Compute: $∂J(\theta_{lookahead})$

$v\theta_t = \beta * v\theta_{t-1} + ( 1 - \beta ) * ∂J(\theta_{lookahead})$

$\theta = \theta - \alpha * v\theta_t$

> *This can also done without the scaling by $(1 - \beta)$ or done as $\beta * v\theta_{t-1} - \alpha * ∂\theta_t$ as previous in [[Momentum]], see [[Interpretations of Momentum]].*

This then allows for the model to conjecture where the optimal jump might be and then correct after making that jump.

Essentially, the $∂J(\theta_{lookahead})$ is added onto the $\beta * v\theta_{t-1}$, as a means of 'correcting' the error that would've been made from purely relying on the past accumulated gradients.

While in regular [[Momentum]], the big jump would be made without any additional correction prior to the next iteration. The jump or weight update, would've just been made based on the current gradient and the accumulated past gradients without any intermediate error-correction.

![[Pasted image 20240703105719.png | 500]]

Note, that when implementing this in practice, you'd need to compute an additional forward pass using the 'lookahead' parameters to get the variables you need to compute the gradients.[^1]

[^1]: At least as was my means of doing so in my implementation from scratch.