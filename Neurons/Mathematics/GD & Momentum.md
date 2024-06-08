Gradient Descent with Momentum involves computing an exponentially weighted average of our gradients and then use that average to update our weights.

It's used when dealing with high curvature (implying lots of local minima), 

Say we had the surface of the loss function as such:
	
![[Screenshot 2024-06-08 at 3.27.08 PM.png]]

and we began to optimize towards the global optima (the red dot)
	
![[Screenshot 2024-06-08 at 3.27.40 PM.png]]

The problem posed here is that to speed up learning, you can't introduce a larger learning rate as that may cause the learning path to further oscillate vertically ultimately slowing down learning.[^1]

What you want is a means to be able to learn *horizontally* towards the optima faster while maintaining a slower *vertical* rate of learning.

So you can implement what's called momentum, which is based on [[Exponentially Weighted Average]]s

1. Compute the original gradients, $\frac{∂L}{∂W}$ ($dw$) and  $\frac{∂L}{∂Bm}$ ($db$)

2. Compute the [[exponentially weighted average]]s 
	$vdw = \alpha \cdot (\beta vdw + (1 - \beta)dw)$
	$vdb = \alpha \cdot (\beta vdb + (1 - \beta)db)$

	>*Making use of $vdw = \beta{vdw} + dw$ works just as fine, though tuning the $\beta$ and $\alpha$ can differ slightly.
	>
	>Also, a $vd\theta$ param is typically called the "velocity" term.

3. Update the weights per:
	$w = w - vdw$
	$b = b - vdw$

Essentially, just as is done in [[exponentially weighted average]]s, we're computing the exponential average of the gradients and using it as a means to update our weights, which then tends to mitigate the *vertical* oscillations in the learning path.

	![[Screenshot 2024-06-08 at 3.48.45 PM.png | 400]]

As can be noticed there, the `ewa` (blue) or the [[exponentially weighted average]]d values have less vertical oscillations than the original `data` (orange).

So we're not updating our weights based on the gradients, but on the [[Exponentially Weighted Average]]d gradients.

So, when implementing this, you now have 2 hyperparameters of 
- Learning rate $\alpha$
- $\beta$ which manages the [[Exponentially Weighted Average]]

[^1]: It slows down like this:

	![[Screenshot 2024-06-08 at 4.05.48 PM.png | 300]] 