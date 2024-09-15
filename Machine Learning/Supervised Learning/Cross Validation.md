- To estimate generalization error, we need data unseen during training. We split the data as
	- Training set - 50%
	- Validation set - 25%
	- Test/Publication set - 25%
- Resampling when there is few data
- From a set of possible hypothesis classes $H_{i}$,
	- Fit each $h_{i} \epsilon H_{i}$ on the training set.
	- Select the hypothesis, hi that is the most accurate on the validation set (cross-validation).
- Validation Set is used to find the best model
- Test set to report the error of the best model

 