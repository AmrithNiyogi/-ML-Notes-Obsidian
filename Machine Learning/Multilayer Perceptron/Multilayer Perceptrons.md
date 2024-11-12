- Can implement non-linear discriminants/ functions of the input
- 2 Layer network
	- Input Layer: Inputs + Bias term
	- Activation propagates in the forward direction and hidden units $z_h$ are calculated
	- $$z_{h} = sigmoid(w^{T}_{h}x)=\frac{1}{1+\exp\left[ -\Big( \sum^{d}_{j=1} w_{hj}x_{j} + w_{h{0}}\Big) \right]}$$
	- where, h:1,...,H
	- Output Layer: takes hidden units as inputs
	- $$y_{i} = v_{i}^{T}z=\sum^{H}_{h=1}v_{ih}z_{h}+v_{i0}$$
	- where $v_{i{0}}$ are bias weights



![[Pasted image 20241112104642.png]]


- Output Layer:
	- Regression: no nonlinearity in the output layer in calculating y
	- Binary classification: one sigmoid output unit
	- K>2 classes: K SoftMax output units as output nonlinearity
- Hidden Layer:
	- Nonlinear activation (e.g., sigmoid, tanh)
	- Hidden units make a nonlinear transformation from the d-dimensional input space to H-dimensional hidden space
	- Multiple layers possible for increased complexity
- Activation Functions:
	- Sigmoid: 0 to 1 range, Tanh: -1 to +1 range
- Differentiable activations enable gradient-based learning
- More layers increase capacity but risk overfitting
- The output layer combination of non-linear basis function values computed by hidden layer