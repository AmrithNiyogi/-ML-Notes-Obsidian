- Perceptron is a basic processing unit
- Input
	- $$x_{j} \ \epsilon \ \Re, \ j=1,\dots,d$$
- Connection/Synaptic Weight
	- $$w_{j} \epsilon \ \Re$$
- Output
	- $$y$$
- Intercept $w_{0}$ to make the model more general
$$y = \sum_{j=1}^{d}w_{j}x_{j} + w_{0} = w^{T}x$$
$$w = [w_{0}, w_{1},\dots,w_{d}]^{T}$$
$$x=[1,x_{1},\dots,x_{d}]^{T}$$
- Learn the weights/parameters to get outputs

![[Pasted image 20240921105112.png]]