- Let $\theta$ as a random variable with prior probability, $p(\theta)$
- Baye's rule:
	- $$p(\theta|X) = \frac{p(X|\theta)p(\theta)}{p(X)}$$
- p(X): [evidence]
	- For continuous $\theta$; $p(x) = \int p(x|\theta)p(\theta)d\theta$
	- For discrete; p(x) = sum of $p(x|\theta)p(\theta)$ for all possible values of $\theta$
- Estimate p(x|X) at a point x for sample X:
	- $p(x|X) = \int p(x,\theta|X) \ d\theta$
	- $p(x|X) = \int p(x|\theta, X) p(\theta|X) \ d\theta$
	- $p(x|X) = \int p(x|\theta) p(\theta|X) \ d\theta$

- Using Maximum a Posteriori (MAP): 
	- $$\theta_{MAP} = argmax_{\theta} \ p(\theta|X)$$
	- $p(x|X) = p(x|\theta_{MAP})$
	- Maximizes posterior
- Maximum Likelihood(ML):
	- $$\theta_{ML} = argmax_{\theta} \ p(X|\theta)$$
	- $\theta_{MAP} \equiv \theta_{ML}$ when prior is flat.
	- Maximizes likelihood
- Baye's:
	- $$\theta_{Baye's} = E[\theta|X] = \int \theta \ p(\theta|X) \ d\theta$$
	- Expected value of the posterior


#### Example
$$x^{t}\sim N(\theta,\sigma^{2)} \ \ and \ \ \theta \sim N(\mu_{0}, \sigma^2_{0})$$
$$p(X|\theta) = \frac{1}{(2\pi)^{\left( \frac{N}{2} \right)}\sigma^{N}}\exp \Biggl[ -\frac{\sum_{t}(x^t-\theta)^2}{2\sigma^2}\Biggr]$$
$$p(\theta) = \frac{1}{\sqrt{ 2\pi }\sigma_{0}}\exp\Biggl[ -\frac{( \theta-{\mu_{0}^2})}{2\sigma^2_{0}} \Biggr]$$
$$It \ can \ be \ shown \ that \ p(\theta|X) \ is \ normal \ with  $$
$$E[\theta|X] = \frac{\frac{N}{\sigma^2}}{{\frac{N}{\sigma^2}} + {\frac{1}{\sigma^{2_{0}}}}}m+{\frac{\frac{1}{\sigma^2_{0}}}{{\frac{N}{\sigma^2}} + {\frac{1}{\sigma^2_{0}}}}\mu_{0}}$$

- This shows that the Bayes’ estimator is a weighted average of the prior mean $μ_0$ and the sample mean m, with weights being inversely proportional to their variances.