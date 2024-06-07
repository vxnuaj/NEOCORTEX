Mini-Batch Gradient Descent is similar to [[Gradient Descent]] in the algorithmic sense, with the difference that it processes smaller batches of the entire dataset prior to taking a training step, rather than processing the entire batch at once and then taking a training step.

This can improve computation time and improve learning speed of a model, especially when there is a large number of training samples in a dataset.

For some intuition, say you have training set $X$.

$X = (784, 60000)$, where there are $784$ features and $60000$ samples.

We can split up $X$ into $6$ mini-batches of $10000$ samples each:

$X^{1} = (784, 10000)$
$X^{2} = (784, 10000)$
$X^{3} = (784, 10000)$
$X^{4} = (784, 10000)$
$X^{5} = (784, 10000)$
$X^{6} = (784, 10000)$

feeding each $X^{t}$ in once and taking a training step in between, then restarting from $X^{1}$ once more.

The trend of the loss function will be less smooth due to the fact that within each forward pass, your model is operating on new unseen samples, but it should still trend downward.

To choose the mini-batch size, it will be in between [[Stochastic Gradient Descent]], where each sample is a 'mini-batch', and batch [[gradient descent]] size, where you get a faster rate of learning whilst maintaining the speed-up effects from vectorization.

>*The former wouldn't allow for a model to converge while the latter provides easier convergence and larger steps without the speed benefit of mini-batch*

- If you have a small training set, make use of batch [[gradient descent]]
	- where $m ≤ ~2000$
- Typical mini-batch sizes are 
	- 64 $\rightarrow$ 1024, on the powers of $2$ given how modern computer hardware runs[^1]
- Make sure your mini-batch fits in your CPU / GPU nmemory


---

[^1]: Many computer systems have architectures that are optimized for accessing data on powers of 2.