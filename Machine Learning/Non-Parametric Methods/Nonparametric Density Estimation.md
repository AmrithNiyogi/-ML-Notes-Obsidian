- Given the training set $X=\{x^{t}\}_{t}$ drawn iid <font color="#4bacc6">(independent and identically distributed) </font>from $p(x)$
- Let $\hat{p}(\bullet)$ estimator of $p(x)$
- CDF (Cumulative Distribution Function) of a random variable X:
	- F(x) = P(X<= x)
	- $$\hat{F}(x) = \frac{\#\{x^{t}\le x\}}{N}$$
- PDF: Derivative of CDF
	- $$\hat{p}(x) = \frac{1}{h}\Bigg[  \frac{{\#\{x^{t}\le x+h\}} - {\#\{x^{t} \le x\}}}{N}\Bigg]$$
	- where, h is the length of the interval


## Example - 

- $$X={151,154,157,159,162,165,167,170,173,175,178,180}$$
	- $$X_{0} = 150,\  h= 5$$
	- estimate density at $x=160$

### Probability Density Function (PDF)

To estimate the density using the **PDF**, we assume the data comes from a normal distribution and use the normal distribution formula:

$$f(x) = \frac{1}{\sqrt{ 2\pi \sigma^2}}*\exp\left[ -\frac{(x-\mu)^{2}}{2\sigma^2} \right]$$
Where:

- $\mu$ is the mean of the dataset.
- $\sigma$ is the standard deviation of the dataset.

1. Calculating the mean of the dataset
$$\mu = \frac{151+154+157+159+162+165+167+170+173+175+178+180}{12}$$
$$\mu = \frac{1911}{12} \approx 159.25$$

2. Calculate the standard deviation
$$\sigma = \sqrt{ \frac{1}{N}  \sum_{i=1}^{N}(x_{i} - \mu)^2}$$
$$(151−159.25)^2=(−8.25)^2=68.06 $$
$$(154 - 159.25)^2 = (-5.25)^2 = 27.56$$$$(157 - 159.25)^2 = (-2.25)^2 = 5.06$$$$(159 - 159.25)^2 = (-0.25)^2 = 0.06$$$$(162 - 159.25)^2 = (2.75)^2 = 7.56$$$$(165 - 159.25)^2 = (5.75)^2 = 33.06$$$$(167 - 159.25)^2 = (7.75)^2 = 60.06$$$$(170 - 159.25)^2 = (10.75)^2 = 115.56$$$$(173 - 159.25)^2 = (13.75)^2 = 189.06 $$$$(175 - 159.25)^2 = (15.75)^2 = 248.06$$$$(178 - 159.25)^2 = (18.75)^2 = 351.56$$ $$(180 - 159.25)^2 = (20.75)^2 = 430.56$$
Now, sum up all the squared differences:
$$68.06+27.56+5.06+0.06+7.56+33.06+60.06+115.56+189.06+248.06+351.56+430.56=1536.20$$

$$\sigma^{2}= \frac{1536.20}{12} = 128.02$$
$$\sigma = \sqrt{ 128.02 } \approx 11.31$$

3. Estimate the density at x = 160
$$(x-\mu)^{2} = (160 - 159.25)^{2} = (0.75)^{2} = 0.5625$$
Dividing by $2\sigma^{2}$
$$\frac{(x-\mu)^{2}}{2\sigma^{2}}= \frac{0.5625}{2*128.02} = \frac{0.5625}{256.04} \approx 0.0022$$
Computing the exponent
$$\exp[-0.022] \approx 0.9978$$
Calculating the coefficient
$$\sqrt{ 2*\pi*\sigma^{2} } = \sqrt{ 2 * \pi * 128.02 } = \sqrt{ 804.79 } \approx 28.37$$
$$\frac{1}{28.37} \approx 0.0352$$
Final calculation
$$f(160) = 0.0352 * 0.9978 \approx 0.0351$$

---

### Cumulative Density Function (CDF)

The **CDF** gives the probability that a value drawn from the dataset is less than or equal to $x$. To estimate the density using the CDF, we can calculate the difference in the CDF over a small interval around $x=160$.

$$F(x) = P(X \le x)$$

To approximate the PDF from the CDF, we compute the finite difference:

$$f(x) \approx \frac{F(x+\Delta x) - F(x - \Delta x)}{2\Delta x}$$, where $\Delta x$ is  small value, such as $\Delta x = 0.5$

1. Estimate $F(160+0.5)$ and $F(160-0.5)$:
	- $$F(160.5) = \frac{8}{12}$$
		- since 8 data points are $\le 160.5$
	- $$F(159.5) = \frac{6}{12}$$
		- since 8 data points are $\le 160.5$
2. Compute the difference

$$f(160) = \frac{F(160.5) - F(159.5)}{2*0.5} = \frac{\frac{8}{12} - \frac{6}{12}}{1} = \frac{2}{12} = 0.1667$$
##### Result:

The estimated density at $x=160$ using the **CDF** approximation is **0.1667**.