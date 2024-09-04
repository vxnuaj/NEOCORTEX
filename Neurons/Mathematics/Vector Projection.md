#LinearAlgebra 

Vector projection is a technique where we take a vector, say $\vec{v}$, and project it onto another vector $\vec{u}$.

It measures the amount by which a given vector goes in direction of another vector.

When $\vec{v}$ is smaller than $\vec{u}$, the projection of $\vec{v}$ onto $\vec{u}$ is a portion of $\vec{u}$, representing the component of $\vec{v}$ that goes in direction of $\vec{u}$.

If $\vec{v}$ and $\vec{u}$ are orthogonal, the projection of $\vec{v}$ onto $\vec{u}$ is essentially $0$.

Say $\vec{p}$ is the projected vector from $\vec{v}$ to $\vec{u}$ where $\vec{p} = k\vec{u}$ and $k$ is a scalar multiple of $\vec{u}$.

- The $\vec{p}$ can be described this way as the projected vector must be going in the same direction as $\vec{u}$

Finding $\vec{p}$ is then a matter of finding the scalar $k$.

This can be done as:

$k = \frac{\vec{v} \cdot \vec{u}}{||\vec{u}||^2}\vec{u}$

and to get the final projection, we multiply it by $\vec{u}$:

$p = k\vec{u}$

When computing the projection of a vector onto another vector, the magnitude of each vector doesn't matter, you'll get the same projection either or.

Then, once we project a vector, $\vec{v}$ onto another vector $\vec{u}$, all we need to know are the multipliers that project the original vector, $\vec{v}$ onto $\vec{u}$, and the values for the vector being projected onto, which is $\vec{u}$.

Doing so reduces the dimensionality of the datapoints, which can prove to be useful computationally if dealing with complex datasets.

Since we're getting estimates, of near equivalent norms, taking the vector projection of near similar yet different datapoints, can significantly decrease the magnitude, as the dimensionality of the given vectors increase.
