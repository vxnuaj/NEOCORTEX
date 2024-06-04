Dropout is a [[Regularization]] technique that eliminates / ignores a specific set of neurons to optimize the network size to reduce overfitting and improve generalizability.

It aims to reduce co-dependence / co-adaptation amongst neurons. Some neurons depend on others to do the 'hard work' while they sit by and not contribute to the overall output.

When you dropout neurons randomly, the 'lazy' neurons must start learning and begin to reduce reliance on the 'hard working' neurons.

In dropout regularization, dropping neurons out means making a set of neurons $0$, based on a probability $p$, and normalizing the rest of the neurons that aren't eliminated.

![[Screenshot 2024-06-04 at 8.23.21 AM.png | 400]]

Another common way to implement dropout is [[Inverted dropout]].