#programming

>*The example is based on the MNIST dataset with class labels from 0 to 9*

To implement [[one hot encoding]] in python, you first create a row or column vector of zeros with a size equivalent to the number of classes in your dataset.

```
one_hot_y = np.zeros((1, np.max(y) + 1))
```

Here, `np.zeros` creates an array of 0s with 1 row and the number of columns equivalent to the number of classes in `y`.

>*In this case, we use +1 to add onto `np.max(y)`, which is 9 given the MNIST dataset, in order to get a column size of 10. If *

