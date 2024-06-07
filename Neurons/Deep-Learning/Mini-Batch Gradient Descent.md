Mini-Batch Gradient Descent is similar to [[Gradient Descent]] in the algorithmic sense, with the difference that it processes smaller batches of the entire dataset prior to taking a training step, rather than processing the entire batch at once and then taking a training step.

This can improve computation time and improve learning speed of a model.

For some intuition, say you have training set $X$.

$X = (784, 60000)$, where there are $784$ features and $60000$ samples.

We can split up $X$ into $6$ mini-batches:

$X^{1} = (784, 10000)$
$X^{2} = (784, 10000)$
$X^{3} = (784, 10000)$
$X^{4} = (784, 10000)$
$X^{5} = (784, 10000)$
$X^{6} = (784, 10000)$

feeding each $X^{t}$ in once, prior to taking a training step.


---

Vectorization allows us to process big sizes of `m` samples quickly. But the great `m` is, the more computation time it takes. 

If we have 5 mil samples, we have to process all 5 mil before one training step

But if we process a smaller batch of samples at a time, the model takes a training step earlier, making learning and computation a bit faster. 