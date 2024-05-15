The Smoothed Cross Entropy Loss, is a variation of the [[categorical cross entropy loss]], but instead takes in an encoded vector that had [[label smoothing]] applied to it.

Similarly to [[categorical cross entropy loss]], it can be mathematically defined as:

$SCE = - \frac{1}{m} \sum Y(\log(\hat{Y}))$, where $m = numsamples$

while in code, alongside [[label smoothing]], it can be defined as:

- [ ] https://proceedings.neurips.cc/paper_files/paper/2019/file/f1748d6b0fd9d439f71450117eba2725-Paper.pdf
- [ ] Definition, Mathematical and Code
- [ ] Derivative, Mathematical and Code
- [ ] Usage in regression, Concept and Implementation
- [ ] Characteristics