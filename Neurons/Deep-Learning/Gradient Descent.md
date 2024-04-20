Gradient descent is an optimization algorithm commonly used in neural networks that involves [[forward propagation]] to get the prediction of a model, [[back propagation]] to get the gradients of the loss w.r.t to params of a model, and then an [[update rule]] to optimize the params of a model through a [[learning rate]] for a specific number of epochs to the global minima of a [[loss function]].

For example, say we had a neural network of:
--- start-multi-column: ExampleRegion1  
```column-settings  
number of columns: 2
largest column: right
border:off
shadow:off
```
$w^1$, of dims ()
$b^1$ 
$w^2$ 
$b^2$ 

--- end-column ---

$n_x = n^0$, corresponding to total input features.
$n^1$, corresponding to number of neurons in hidden layer.
$n^2$, corresponding to number of neurons in the output layer


--- end-multi-column

