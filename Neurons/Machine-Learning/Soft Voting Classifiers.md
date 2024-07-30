An extension of [[Majority Voting Classifiers]], but where instead of computing the hard majority, we compute the soft majority, based on the output probabilities of a decision tree to a given class.

For each model $f_i$, rather than outputting the raw label as a prediction, it would output the probability of a sample $X$ belonging to a label $Y$.

This probability would then be used to compute an average probability of a given $X$ belong to $Y$, for all classes in $Y$ using a weight $w_i$ which is typically the same across all predictions as $\frac{1}{n}$ where $n$ is the total number of models.

The final probability is then computed as:

$\hat{Y} = argmax(\sum_{i = 0}^n w_i \cdot p_{ij})$

> *Here, if we have a given classifier with a higher reliability, we can increase the prominence of it's classification by increasing the magnitude of it's corresponding weight.*
> 
> *Then, the classifier has more of a say into which is the right prediction within the overarching ensemble*
> 
> *Finding these weights might prove to be tedious, it's a form of hyperparameter tuning. You might be able to do a grid / random search.*

Then, the class belonging to the highest probability is chosen as the class prediction.