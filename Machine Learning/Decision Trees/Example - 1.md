- Using IREP:
	- "If Income is High and Employment Status is Employed, then Loan Approved = Yes." 
	- Pruned Rule: 
		- If Income is High, then Loan Approved = Yes."
	- Continues till all positive examples are covered


- Using Ripper:
	-  Initial Rule: 
		- "If Income is High, then Loan Approved = Yes."
	- Optimized Rule: 
		- "If Income is High and Credit Score is Excellent or Good, then Loan Approved = Yes."
	- Continues to add new rules till classification error is minimum
	- Final Rule Set:
		- Rule 1:
			- "If Income is High and Credit Score is Excellent or Good, then Loan Approved = Yes."
		- Rule 2: 
			- "If Income is Low and Credit Score is Poor, then Loan Approved = No."


![[Pasted image 20240918172813.png]]
