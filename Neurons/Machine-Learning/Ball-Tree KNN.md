The Ball-Tree KNN is defined by taking a given point, $X$, as a pivot point which denotes the center of the first ball, and computing another point $Y$ with the furthest distance from the point $X$

Then another point $Z$ is computed from $Y$ which is the furthest from $Y$.

Then 2 circles or 'balls' which serve as the split segments of the tree are created with the points $Y$ and $Z$ as the center and the radius being the distance from center point $X$ to each point $Y$ and $Z$ respectively.

This process is repeated within each segment until each ball reaches the minimum number of samples defined by a parameter called the leaf-size.
