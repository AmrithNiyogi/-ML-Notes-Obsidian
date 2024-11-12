- Training of Multilayer perceptron is the same as a perceptron; but the output is a nonlinear function of inputs in multilayer perceptron
- Taking hidden units as inputs, the second layer is a perceptron and parameters $v_{ij}$ are updated given inputs $z_{h}$
- For first-layer weights $w_{hj}$, apply the <font color="#9bbb59">chain rule</font> to calculate gradient:
![[Pasted image 20241112114115.png]]

- Error propagates backwards from output y to inputs, hence the name "<font color="#9bbb59">backpropagation</font>"

![[Pasted image 20241112114129.png]]
