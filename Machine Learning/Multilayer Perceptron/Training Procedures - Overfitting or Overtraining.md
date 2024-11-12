- Number of weights: H (d+1)+(H+1)K
- Complexity: O(H · (K + d)) for space and time
- Training time: O(e · H · (K + d)), e = number of epochs
- Complexity depends on number of hidden units (H)
- Overcomplex Models
	- Too many hidden units lead to poor generalization
	- Similar to overfitting in polynomial regression
- Overtraining Phenomenon
	- Training error decreases with epochs
	- Validation error increases after certain point
- Causes
	- Weights move away from 0 as training progresses
	- Effectively increases model complexity over time, leads to poor generalization
- Mitigation Strategies
	- Early stopping based on validation error
	- Optimal hidden unit selection via cross-validation
	- Multiple training runs with different initializations


![[Pasted image 20241112105808.png]]

![[Pasted image 20241112105827.png]]

