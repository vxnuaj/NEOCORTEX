 Exponentially weighted averages is a type of [[moving average]] with the weights, $W$, exponentially decreasing as datapoints get older rather than linearly decreasing or being arbitrarily assigned.

It's formula is computed as:

$V_t = \beta V_{t-1} + (1 - \beta) \theta_t$

	The lower $\beta$ is, the more priority the EWA gives to more recent datapoints allowing for more accuracy with a downside of less smoothing and increasing amount of random noise.

	![[Screenshot 2024-06-08 at 9.11.07 AM.png | 500]]

If for example, we were computing the EWA of $V_{10}$ within a set of 10 datapoints, with a $\beta$ value of $.95$ it'd look as such:

$V_{10} = (.05)\theta_{10} + (.95)V_{9}$

$V_{10} = (.05)\theta_{10} + (.95)(.05(\theta_9) + (.95^2)V_8)$

$V_{10} = (.05)\theta_{10} + (.95)(.05(\theta_9) + (.95^2)(.05(\theta_8) + (.95^3)V_7))$

each $V_n$ having it's own EWA calculation, with the $\beta$ value exponentially decreasing as older datapoints are presented.