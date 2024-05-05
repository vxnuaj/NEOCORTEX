#mathematics 

Typically, if $w_1$ is set to the dimensions of $(n_1, inputs)$, where $n_1$ is the number of neurons in a layer, the dimensions for the rest of the parameters can be set as:

$w^{[l]}: (n^{[l]}, n^{[l-1]})$
$b^{[l]}: (n^{[l]}, 1)$

and the dimensions of the gradients will the same as their respective parameters,

$dw^{[l]}: (n^{[l]}, n^{[l-1]})$
$db^{[l]}: (n^{[l]}, 1)$

where $l$ is the current layer.

Essentially, the dimensions of a given layer are defined as the first dimension being equivalent to the number of neurons in the current layer $(l)$ and the columns being equivalent to the number of neurons in the previous layer $(l-1)$

