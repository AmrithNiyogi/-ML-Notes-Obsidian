- Find latent factors that influence the observable variables, x; find correlation between variables
- Aim to model the data into smaller dimensional space without loss of information
- Unsupervised technique
- Let, X sample drawn from some probability density, $E(x) = \mu$ and $Cov(x) = \sum$

Assume latent factors are unit normals; $E[z_{j}]=0$, $Var(z_{j})=1$, $Cov(z_{i}, z_{j})=0$ and $i \neq j$
Let added source of each input (noise) $\varepsilon_{j}$ such that 

$$E[\varepsilon_{j}]=0, \ Var(\varepsilon_{j})= \psi_{j}); \ Cov(\varepsilon_{i}, \varepsilon_{j})=0, \ Cov(\varepsilon_{j}, z_{j})=0$$

FA assumes each input dimension $x_{i}$ is the weighted sum of k(<d) factors + residual term

$$x_i - \mu_i = v_{i1}z_1 + v_{i2}z_{2}+\dots +v_{ik}z_{k} + \epsilon_{i} \forall i = 1, \dots , d$$
$$x_{i} - \mu_{i} = \sum_{j=1}^{k}v_{ij}z_{j} + \epsilon_{i}$$
**Vector-matrix form:**
$$x-\mu = Vz + \varepsilon$$, where V: dxk matrix of weights [ Factor loadings]


- Example with 2 factors:
- $$Cov(x_{1}, x_{2}) = v_{11}v_{21} + v_{12}v_{22}$$
- if $x_{1}$ and $x_{2}$ have high covariance, then they are related through a factor.
	- If it is the first factos, theb $v_{11} \ and v_{21} \ w$ 
- If the covariance is low, then $x_{1} \ and  \ x_{2} \ depend \ on \ different \ factors$
	- In the products in the sum, one term will be high and the other will be low and the sum will be low.