A cyclical learning rate is a learning rate schedule that varies between minimum and maximum bounds.

These minimum and maximum bounds are set based on a conjecture of what the optimal learning could be.

The idea is that while the learning rate cycles between the minimum and maximum bounds, it'll spend some time and the optimum learning rate, and a good amount of time right around the optimum learning rate.

This cyclical learning rate can help a model escape local minima, explore different regions of the loss space, and may reduce the need for tuning the learning rate through exhaustive methods such [[grid search]].

This method can be combined with applying [[Exponential Decay]] to the general minimum and maximum bounds, to allow the model shrink it's learning rate while still using a cyclical method.