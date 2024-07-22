When based on the [[information gain]] and the [[weighted entropy]] / [[Entropy]] on a binary split.

1. Choose a [[Split Feature]] to split the data upon
2. Then consider all possible splits of that feature, based on the [[Splitting Threshold]]
3. Compute baseline [[entropy]] for both splits 
4. Compute the [[weighted entropy]] for the given splits 
5. Compute the [[Information Gain]] for the given splits 
6. Do this for all splits 
7. Choose the best split, that maximizes information gain or minimizes weighted entropy