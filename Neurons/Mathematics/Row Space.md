#LinearAlgebra 

The row space, or $Row()$ denotes the possible space or span of the rows of a given matrix $A$.

If we had a matrix:

$A = \begin{pmatrix} 1, 2 \\ 4, 3 \\ 9, 2 \end{pmatrix}$

The individual rows would be $\begin{pmatrix}1, 2 \end{pmatrix}$, $\begin{pmatrix}4, 3 \end{pmatrix}$, and $\begin{pmatrix}9, 2 \end{pmatrix}$.

Let's call them $a$, $b$, and $c$ correspondingly.

Then, the $Row()$ is the possible span that can be covered by a linear combination of $a$, $b$, and $c$, provided that they are linearly independent.

When computing a linear combination amongst the row space, we then treat each row vector as a separate "column" in the [[Column Picture]] and the [[Row Picture]].

Or the row space can then be seen as the column space of the transpose of $A$, as $A^T$