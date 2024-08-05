#LinearAlgebra

Elimination matrices serve as a means to reduce a matrix, $A$, to it's upper triangular form or [[Row Echelon Form]] or [[Reduced Row Echelon Form]], denoted as $U$. 

The inverse of an elimination matrix, $E^{-1}$ can be used to take $U$ and convert it back to $A$ as:

$E^{-1}U = A$

though only if the inverse of $E$ was derived when $E$ was a matrix multiplication of all other intermediary elimination matrices $E_i$. 

$E = E_kE_{k-1}...E_2E_1$

Otherwise, the matrix would not yield back $A$, but instead an intermediary matrix between $A$ and $U$, say a $U_i$.
