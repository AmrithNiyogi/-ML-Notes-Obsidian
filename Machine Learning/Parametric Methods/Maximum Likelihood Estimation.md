- Find the parameter values, $\theta$ that makes the observed data most likely
- Independent and Identically Distributed (IID) samples $X = \lbrace x^t \rbrace^N_{t=1}$
	- where, $x^{t}\sim p(x|\theta)$
- Likelihood of $\theta$ given the sample, X
	- $$l(\theta|X) \equiv p(X|\theta) = \prod_{t=1}^{N}p(x^t|\theta)$$
- Log likelihood:
	- $$L(\theta|X) \equiv \log l(\theta|X) = \sum_{t=1}^{N}\log p(x^t|\theta)$$
- Maximum likelihood estimator (MLE):
	- $$\theta^{*}= argmax_{\theta}L(\theta|X)$$


