Decision Trees are a type of model that makes use of binary or multiway decisions to converge on a decision that's optimal for the given situation.

Given a datapoint, at each node of a decision tree, there must be a binary or multiway decision path where the tree splits off into other nodes or perhaps leaves that represent a final decision.

The depth of a decision tree defines the length of the longest path from the root node to a leaf node.

- A shallow tree might under-fit data.
- A deep tree might over-fit the data.

![[Screenshot 2024-07-20 at 7.44.41 AM.png | 400]]

The root node is the first node while the leaf nodes represent the final decision or output. The internal decision nodes are the intermediary nodes that represent intermediary decisions between a root node and a leaf node. Branches are what connects the nodes.

The decision tree continues to split until a node is ***pure***, meaning one class remains, a ***maximum depth*** is reached, a ***minimum sample size*** is reached, or a ***performance metric***, say Entropy, is achieved.

There are different types of splitting criteria for a decision tree, such as the [[Gini Impurity]] or [[Entropy]]

> *See [[Splitting a Decision Tree]], note that it is a recursive algorithm*

[[Greedy Search]] can be used to find the optimal decision path for a tree, based on the maximum information gained from the split.

Decision Trees can tend to have high variance and overfit, given that it's non-parametric and is very flexible. 

The solution to this is to prune the tree perhaps via maximum depth or a performance metric such as classification error or [[information gain]].

Benefits of decision trees include the absence of a need for pre-processing and being able to handle all types of data.