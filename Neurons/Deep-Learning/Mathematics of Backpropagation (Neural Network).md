
>*Assuming the typical use of [[categorical cross entropy]] and [[ReLU]]*
>
>*This is the simplified derivation of the chain rule.*

The backpropagation for a given layer in a vectorized format, where $l$ is the current layer is as follows:

$dZ^l = dA^l * dG^l(Z^l)$
$dW^l = dZ^l \cdot A^{[l-1]T} * \frac{1}{m}$
$dB^l = \frac{1}{m} * \sum dZ^l$
$dA^{[l-1]} = W^{[l]T} \cdot dZ^l$


![[Screenshot 2024-05-05 at 11.59.43 AM.png]]