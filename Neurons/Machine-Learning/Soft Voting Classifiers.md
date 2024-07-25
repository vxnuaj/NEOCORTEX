An extension of [[Majority Voting Classifiers]], but where instead of computing the hard majority, we compute the soft majority, based on the output probabilities of a decision tree to a given class.

For each model $f_i$, rather than outputting the raw label as a prediction, it would output the probability of a label $Y$ belonging to a sample $X$.

This probability would then be used to compute an average probability of a given $X$ belong to $Y$, for all classes in $Y$.

Then, the class belonging to the highest probability is chosen as the class prediction.