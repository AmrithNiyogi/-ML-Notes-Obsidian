- Improve the performance of gradient descent using the following techniques:
- <font color="#9bbb59">Momentum</font>
	- α typically between 0.5 and 1.0
	- Benefits:
		- Smooths oscillations
		- Improves convergence speed
	- Drawback: Requires extra memory

$$\Delta w^{t}_{i} = -\eta\frac{{\partial E^{t}}}{\partial w_{i}} + \alpha \Delta w_{i}^{t-1}$$

- <font color="#9bbb59">Adaptive learning rate</font>
	- η takes between 0.0 and 1.0, mostly η <= 0.2
	- Dynamically adjusts learning rate η
	- Increases η when error decreases
	- Decreases η geometrically when error increases
	- Consider using average error over past few epochs


$$\Delta \eta = \Bigg\{ \begin{matrix}
+a & if \ E^{t+r} < E^t \\
-b\eta & otherwise
\end{matrix}$$

