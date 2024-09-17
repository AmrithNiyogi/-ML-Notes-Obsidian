- Naïve Estimator: Independent of origin $x_0$
$$\hat{p}(x) = \frac{\#\left\{ x-\frac{h}{2} < x^{t} \le x + \frac{h}{2} \right\}}{Nh}$$
$$or$$
$$\hat{p}(x) = \frac{1}{Nh}\sum_{t=1}^{N}w{\frac{(x-x^{t})}{h}}$$

$$w(u) = \Bigg\{\begin{matrix}
1 & if \ |u| < \frac{1}{2} \\
0 & otherwise
\end{matrix}$$


![[Pasted image 20240917190200.png]]


## Example - 

- $$X={151,154,157,159,162,165,167,170,173,175,178,180}$$
	- $$X_{0} = 150,\  h= 5$$
	- estimate density at $x=160$

The **naive estimator** uses a simple uniform box function. If a point is within a certain range $h$ from the given value $x$, it contributes to the density estimate. The naive estimator formula is:

For each point $x^{t}$ in the data, we will compute $\frac{x - x^{(t)}}{h}$​ and apply the box function to decide whether the point contributes to the density estimate. Specifically, if the point $x^{t}$ lies within the interval $[x - \frac{h}{2}, x + \frac{h}{2}]$, it contributes to the estimate.

The interval around $x=160$ with bandwidth $h=5$ is:

$$\left[ 160 - \frac{5}{2} , \ 160 + \frac{5}{2}\right] = [157.5, 162.5]$$
Now, we check which data points from $X$ lie within this interval

Data points: 
$$\{151,154,157,159,162,165,167,170,173,175,178,180\}$$
The points within $[157.5,162.5]$ are - 
$$\{159,162\}$$
Now we compute the estimate using the formula -

$$\hat{p}(160) = \frac{1}{Nh}\sum_{t=1}^{N}w\left( \frac{{160-x^{t}}}{5} \right)$$

$$\hat{p}(160) = \frac{1}{12*5}*2 = \frac{2}{60} = 0.0333$$