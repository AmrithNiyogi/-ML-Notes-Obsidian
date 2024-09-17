- Estimate class-conditional probabilities, $p(x|C_{i})$ and use Baye's rule to get discriminant function


- For <font color="#f79646">Kernel Estimator</font>
	- $$\hat{p}(x|C_{i}) = \frac{1}{N_{i}h^{d}}\sum_{t=1}^{N}K\left( \frac{{x-x^{t}}}{h} \right)r^{t}_{i}$$
	- Estimator of Prior Density
	$$\hat{P}(C_{i}) = \frac{N_{i}}{N}$$
	- Discriminant Function
	$$g_{i}(x) = \hat{p}(x|C_{i})\hat{P(C_{i})}$$
	$$g_{i}(x) = \frac{1}{Nh^{d}}\sum_{t=1}^{N}K\left( \frac{{x-x^{t}}}{h} \right)r^{t}_{i}$$
	- x is assigned to the class for which g(x) is maximum



- For <font color="#8064a2">k-NN Estimator</font>
$$\hat{p}(x|C_{i}) = \frac{k_{i}}{N_{i}V^{k}(x)}$$
	- $k_{i}$ is the number of neighbors out of k nearest that belong of class $C_{i}$
	- $V^k(x)$ is the volume of the d-dim hypersphere centered at x with radius r
	- $r = ||x-x_{(k)}||$ is the distance between x and kth nearest neighbor to x
	- Volume - 
	$$V^{k}=r^{d}c_{d}$$
		- $c_{d}$ is the volume of the unit sphere in d dimensions, for example, $c_{1} = 2, c_{2} = \pi,c_{3} = 4\pi/3$, and so on..
	- Using Baye's Theoem,
	$$\hat{P}(C_{i}|x) = \frac{\hat{p}(x|C_{i})\hat{P}(C_{i})}{\hat{p}(x)} =\frac{k_{i}}{k}$$
		- k-NN assigns input to the class having most examples among k-neighbors