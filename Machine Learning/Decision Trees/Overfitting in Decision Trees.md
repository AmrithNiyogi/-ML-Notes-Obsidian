- If there is noise in data, then growing tree until its purest will result in very large tree which will overfit
	- Very high accuracy on training data, low accuracy on test data


- Techniques to prevent overfitting - 
	- Pruning
		- Post Pruning:
			- After tree is fully grown, remove branches with little importance
		- Pre Pruning:
			- Stop growing tree once it reaches a certain depth
	- Cross-Validation
		- to tune hyper parameters like tree-depth, min number of samples per leaf, etc.
	- Random Forest / Bagging
		- Use multiple trees on random subsets of data and average their predictions 

