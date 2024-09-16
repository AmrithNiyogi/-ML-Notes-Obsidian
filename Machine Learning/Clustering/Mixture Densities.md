- $$p(x) = \sum_{i=1}^{k}p(x|\mathrm{G}_{i})P(\mathrm{G}_{i})$$
	- where, 
		- $\mathrm{G}_{i} \to$ components/groups/clusters
		- $k \to$ hyperparameter
		- $P(\mathrm{G}_{i}) \to$ mixture proportions (priors)
		- $P(x|\mathrm{G}_{i}) \to$ component densitites
- Assume, Gaussian mixture where $p(x|G_{i}) \sim N\left( \mu_{i}, \sum_{i} \right)$ then parameters $\phi = \left\{ P(G_{i}), \mu_{i}, \sum_{i} \right\}_{i=1}^{k}$
- Now, we have an unlabeled sample $X+\{x^{t}\}_{t}$ <font color="#4bacc6">(unsupervised learning):</font>
	- First estimate labels, then estimate parameters of components
- Algorithms – k-means clustering; EM (Expectation Maximization) Algorithm