#processing

One hot encoding is a technique used to represent categorical values into binary values that are understandable for a model.

Differentiating from [[label encoding]], one hot encoding converts variables into binary vectors with a size equivalent to the total number of classes.

>*For example, if I was using the MNIST dataset and wanted to one hot encode the labels, I'd initially create a vector of size 10 as such: $\begin{bmatrix} 0,0,0,0,0,0,0,0,0,0 \end{bmatrix}$*

Within the binary vector, each class in a dataset is represented by a unique binary value of 1 whilst the others remain to be 0.

> *Using the example of the MNIST dataset, if I wanted to represent the label 2 in a one hot encoded format it'd look as such: $\begin{bmatrix} 0,0,1,0,0,0,0,0,0,0 \end{bmatrix}$*
> 
> *If I wanted to represent the label 5, it'd look as such $\begin{bmatrix} 0,0,0,0,0,1,0,0,0,0 \end{bmatrix}$*

We use one hot encoding to avoid [[label leakage]]. Otherwise, our model would learn to assign weights of higher value to predict labels of higher value which would ultimately throw off how our model trains [^1]

[[Implementing One Hot Encoding in Python]]

[^1]: See [[label leakage]]