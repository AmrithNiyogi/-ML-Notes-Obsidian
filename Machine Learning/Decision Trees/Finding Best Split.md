1. Compute impurity measure (P) before splitting
2. Compute impurity measure (M) after splitting
	- Compute the impurity measure of each child node
	- M is the weighted impurity of the children
1. Choose the attribute test condition that produces highest gain
$$Gain = P - M$$
		or equivalently, lowest impurity measure after splitting (M)