If there are more equations than variables in a [[Systems of Linear Equations]], the system is said to be overdetermined and inconsistent unless it's equations do not contradict with each other.

> *Inconsistent meaning there isn't one set of values of the unknowns that satisfies each equation for it's output $B$ in the space of $\mathbb{R}^n$. It has no one solution.*

$\begin{cases} x + y = 2 \\ 2x + 2y = 4 \\ x + y = 3 \end{cases}$

This means that a system has been over constrained, as there are more equations than the number of unknowns, there are more limits to what the values can represent.

Therefore, the supposed $Col()$ or $Row()$ of the space that is supposed to span all $\mathbb{R}^n$ matrices, gets limited below such.

If the equations do not contradict each other, it's consistent yet still over determined. This means that a set of equations within the system can be linearly dependent on another (set of) equation.

$\begin{cases} x + y = 2 \\ 2x + 2y = 4 \\ 3x + 3y = 6 \end{cases}$

Here where the third equation is a summation of the first two.