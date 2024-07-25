Classifiers that leverage majority voting to make a final prediction are a form of [[Ensemble Learning]].

Majority voting classifiers are made up of multiple distinct classifiers, say $f_i$ where $i$ is the $ith$ classifier.

All $i$ classifiers are trained on the same data, to then make a final prediction of $\hat{y}_i$.

For every $\hat{y}_i$ that is made, the majority or the $mode()$ of all predictions is taken to find the majority vote, which is then set as the final prediction, $\hat{Y}$.

We use majority voting to mitigate the impact of that [[Irreducible Error]][^1] has per each individual classifier $f_i$. If the [[Irreducible Error]] is uncorrelated amongst all $i$ models, taking the $mode()$ of all $\hat{y}_i$ can potentially yield a more accurate $\hat{Y}$.

The error for an ensemble model can then be computed using the [[Binomial Theorem]], as:

$\epsilon_{ens}= \sum_{k = 0}^n \begin{pmatrix}n \\ k \end{pmatrix} (1 - \epsilon)^{n - k} \epsilon^k$

where $\epsilon_{ens}$ is the [[irreducible error]] a sum of the binomial probability over all $n$ models and $k$ are the amount of models that predict the sample label.

[^1]: Or in [[Bayes Classifier]]s, the [[Bayes Error]].