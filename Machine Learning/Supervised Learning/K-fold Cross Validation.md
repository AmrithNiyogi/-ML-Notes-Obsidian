- The dataset X is divided randomly into K equal-sized parts, $X_{i}$ , $i = 1,2,3,4\dots..K$
- To generate each pair,
	- one of the K parts is considered as the validation set
	- combine the remaining K − 1 parts to form the training set.
- Doing this K times, we get k pairs:
	 $V_{1} = X_{1}$       $T_{1} = X_{2} \cup X_{3} \cup \dots.. \cup X_{k}$
	 $V_{2} = X_{2}$       $T_{2} = X_{1} \cup X_{3} \cup \dots.. \cup X_{k}$
		 $\vdots$
	 $V_{k} = X_{k}$       $T_{k} = X_{1} \cup X_{2} \cup \dots.. \cup X_{k-1}$
