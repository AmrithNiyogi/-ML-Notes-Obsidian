- Hints: Known properties of the target function, independent of training examples
- Invariance to translation, rotation, size
- Methods of Incorporating Hints
	- Virtual examples
	- Preprocessing
	- Network Structure
	- Modified Error Function
		- Invariance Hint: If x' (virtual example of x) and x are the “same”: $E_{h}=[g(x|θ)- g(x'|θ)]^2$
		- Augmented error: $E'=E+λ_{h} E_{h}$ and $λ_h$: weight of the hint penalty (Abu-Mostafa 1995)
		- Approximation hint:
			- (Fig 1)
	- Tangent Prop: Allow parameter movement along this line of transformation


![[Pasted image 20241112105236.png]]
Fig 1