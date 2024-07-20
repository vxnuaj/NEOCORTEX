The splitting criteria for the original CART decision tree algorithm.

It's used to quantify the impurity or disorder of a set of elements.

It is defined as:

$G = \sum_{i = 1}^K p_i(1 - p_i)$

where it's interval is in the range $[0, .5]$

while for binary classification, it is defined as:

$G = p_1 ( 1 - p_1) + p_2(1-p_2)$