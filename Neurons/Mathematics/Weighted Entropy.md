#stats 

Weighted Entropy is the weighted average of entropy of all subset scenarios in a specific situation.

It's weighted by the proportion of instances in each subset relative to the total dataset size.

$\sum_{j=1}^n\frac{D_j}{|D|}H(D_j)$

where $n$ is the number of total subsets, $D$ is the total size of the dataset, $D_j$ is the number of total instances in the given subset of the dataset, $H(D_j)$ is then the entropy of the given $D_j$. 

---

