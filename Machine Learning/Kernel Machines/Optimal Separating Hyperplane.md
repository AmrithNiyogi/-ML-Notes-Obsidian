- Consider 2-class problem:
![[Pasted image 20241112130156.png]]

- For all training instances to be correctly classified:
	- When $r_{t} = +1$: $w^{T}x_{t} + w_{0} > 0$ 
	- When $r_{t} = -1$: $w^{T}x_{t} + w_{0} < 0$
- Can be re-written as:
$$r_{t}(w^{Tx_{t}}+ w_{0}) \ge 0$$
- Aim is to find $w^T$ and $w_{0}$ such that the functional margin is positive.
- Objective of SVM: In the Hypothesis space of lines, identify the line that maximizes the minimum functional margin (Optimal Separating Hyperplane).