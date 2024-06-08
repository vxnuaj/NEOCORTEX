A moving average is a calculation that allows us to analyze various data points by creating an average of different portions of the dataset, ultimately filtering out random noise from random price fluctuations.


	![[Pasted image 20240608084728.png| 500]]

A simple moving average can simply be calculated by the formula:

$\frac{A_1 + A_2 + ... + A_n}{n}$

where $n$ is the total number of datapoints.

A weighted moving average can be calculated by:

$A_1W_1 + A_2W_2 + ... + A_nW_n$

where a given $W$ is a weight assigned to a specific datapoint at $n$