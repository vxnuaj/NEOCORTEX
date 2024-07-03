---
undefined: 
File: Incorporating Nesterov Momentum into Adam
---
#researchpaper 

> *[Original Paper](https://cs229.stanford.edu/proj2015/054_report.pdf)*

**Intro**

There are many means to which one can improve the performance of a neural network, as:
- Adding [[LSTM]] units rather than relying on simple recurrent units
- Improve initialization through [[Xavier Initialization]] or [[He Initialization]].
- Introducing sparsity through [[L1 Regularization]].
- Modifying the optimizer, i.e., [[RMSprop]].
- Attempting to use second order optimizers.

This paper introduces another means to do so, byt introducing [[Nadam]].

**Related Work**

- *[[Gradient Descent]]* very simple well known and robust
- *Classical Momentum*, implementing a decaying gradient with a const



