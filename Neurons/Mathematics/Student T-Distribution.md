#stats 

A distribution that serves as a means of modeling data without knowing the population $\sigma$ and instead relies purely on the data.

It's PDF is defined as:

$\frac{\Gamma(\frac{v+1}{2})}{\sqrt{\nu\pi}\Gamma(\frac{\nu}{2})}(1 + \frac{t^2}{\nu})^{-\frac{\nu + 1}{2}}$

where $\frac{\Gamma(\frac{v+1}{2})}{\sqrt{\nu\pi}\Gamma(\frac{\nu}{2})}$ is the normalization constant, ensuring that the integral of the entire area under the distribution is equal to $1$, and $(1 + \frac{t^2}{\nu})^{-\frac{\nu + 1}{2}}$ is the function itself that draw the bell curve.