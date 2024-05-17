Xavier Initialization is a form of [[Weight Initialization]], proposed by Xavier Glorot and Yoshua Bengio.

This type of initialization is typically used with the [[Tanh]] function. 

While [[Tanh]] is more robust against vanishing gradients when compared to [[Sigmoid]], it's still prone to vashing gradients if the inputs are very large, positive or negative. 

Initializing model weights using Xavier Initialization helps improve on [[Tanh]] and mitigate the vanishing gradient problem.


---
- [ ] https://proceedings.mlr.press/v9/glorot10a/glorot10a.pdf
- [ ] Motivation / Purpose
- [ ] Formula / Mathematical Rationale
- [ ] Code Implementation
- [ ] Advantages / Disadvantages