- Regression:
	- $W_{ij}$ is the weight from input $x_{j}$ to output $y_{i}$
	- $W$ is the $k \ X(d+1)$ weight matrix

$$y_{i} = \sum_{j=1}^{d}w_{ij}x_{j} + w_{i)} = w_{i}^{T}x$$
$$y=Wx$$
- Classification:
	- Two-Stage Process (Single Layer):
		- Stage 1:
			- Weighted sums calculates linear combinations for each class
		- Stage 2:
			- SoftMax Activation converts outputs to probabilities


$$o_{i} = w^{T}_{i}x$$
$$y_{i} = \frac{\exp 0_{i}}{\sum_{k} \exp 0_{k}}$$
choose $C_{i}$ if $y_{i}=max_{k} \ y_{k}$
![[Pasted image 20240921112611.png]]