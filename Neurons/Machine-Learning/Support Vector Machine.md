A linear support vector machine is a linear classifier, based on a [[maximal margin hyperplane]] that aims to draw a boundary between a set of datapoints, based on a linear decision boundary and "[[Support Vectors]]".

> *Note that support vector machines can be extended to [[Non-Linear Support Vector Machine]]s via the [[Kernel Trick]].*
> 
> *There are also [[Primal Form]] and [[dual form]] for SVMs.*

The goal of a support vector machine is to find the line or hyper plane of a decision boundary that best separates the classes.

The SVM then, aims to classify datapoints based on how they deviate from the line or hyper plane of a decision boundary.

> *In a 2-dimensional space, a line is suitable. In $n$ dimensional spaces, where $n > 2$, a hyperplane is needed.*

We want to find the [[Support Vectors]] which correspond to the largest gap, in the case of SVMs with [[soft margins]], [^1] between the decision boundary and the datapoints by minimizing the [[Hinge Loss]]. Here, this margin would be defined by regularization [^2].

In the case of SVMs with [[hard margins]] we find the datapoints that would lie as close to the support vectors as possible, with a default margin of $1$.

The decision boundary is defined as $w \cdot x + b = 0$.

To classify predictions, if the SVM bases it's binary classifications based on the sign of an output. 

If the prediction of an SVM $f(x)$ is $>0$, the prediction class is $+1$, while if $f(x) < 0$, the prediction class is $-1$.

The weights $w$, represent the distance of the hyperplane or decision boundary that separates the classes in $x$ as best as possible from the corresponding [[support vectors]]. They yield the coordinates of a vector [[orthogonal]] to the hyper plane.

> *[[Orthogonal]] meaning the vectors are perpendicular. 
> $w \cdot x$ if $x$ is the hyperplane, will yield $0$*

Therefore the $L_2$ norm of $w$, as $||w||$, will yield the distance between the decision boundary and it's corresponding [[Support Vectors]].

If we have $w$ as:

$w = \begin{pmatrix} 3 \\ 0 \end{pmatrix}$

and $x$ as:

$x = \begin{pmatrix} 6 \\ 4 \end{pmatrix}$

then within the equation of an SVM as $w \cdot x + b$, the dot product of $w$ and $x$ yields $18$.

Assuming that $b$ is $0$, the prediction of the SVM is $18$. Thereby, given that the prediction is positive, the class predicted is $+1$.

The margin between the optimal line or decision boundary and a given datapoint is called the geometric margin, computed as the [[Euclidean Distance]] defined as:

$\gamma = \frac{y_i(w^Tx_i + b)}{||w||}$

where the numerator represents the predicted vector derived from the boundary $w$, inputs $x$, and bias $b$.

The denominator scales the input down based on the euclidean norm of $w$ or the distance from the decision boundary to the [[Support Vectors]]. This makes sure that when computing the geometric mean, the input $x$ is independent to scaling by $w$.

A support vector machine can be sensitive to outliers, where if a single datapoint of a different class is grouped near to datapoints of different classes, then the decision boundary and [[support vectors]] will skew, indicating a level of overfitting.

Thereby, we can rely on [[Regularization for SVMs]], similar to [[L2 Regularization]] where we add an additional loss penalty to the [[hinge loss]].

[^1]: Winston terminology -- the 'street' 
[^2]: [[Regularization for SVMs]]

___


- [x] Hard Margin SVMs
- [ ] Soft Margin SVMs
- [ ] Non-Linear SVMs.
