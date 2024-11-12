
![[Pasted image 20241112113822.png]]

- First layer weight update ($\Delta w_{hj}$) depends on second-layer weight ($v_{h}$)

- Error Backpropagation:
	- Error term for hidden unit: $(r_{t}-y_{t}) * v_{h}$
	- Weighted by hidden unit's "responsibility" ($v_{h}$)
- Sigmoid Derivative: $z_{h}(1 - z_{h})$ in the weight update equation
- Interdependence of Layers: First-layer weight update uses second-layer weights
- Weight Initialization:
	- Small random values (e.g., [-0.01, 0.01])
	- Prevents sigmoid saturation
- Learning Approaches:
	- Batch learning: Update after full dataset pass
	- Online learning: Update after each pattern (stochastic gradient descent)
		- Converges faster
- Training Process:
- Epoch: Complete pass over training set
- Gradually improves fit to underlying function

![[Pasted image 20241112113550.png]]
