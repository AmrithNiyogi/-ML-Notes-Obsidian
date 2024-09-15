- $p(x) = N (\mu, \sigma^2)$
	- $$p(x) = \frac{1}{\sqrt{2\pi }\sigma}\exp\left[ -\frac{(x-\mu)^2}{2\sigma^2} \right]$$
- Log Likelihood:
	- $$L(\mu, \sigma|X) = -\frac{N}{2}\log(2\pi) - N\log \sigma - \frac{\sum_{t}(x^t-\mu)^2}{2\sigma^2}$$
- MLE:
	- mean:
	- $$m \ or \ \mu= \frac{\sum_{t}x^t}{N}$$
	- variance:
	- $$s^{2} \ or \ \sigma^2= \sum_{t} \frac{(x^t-m)^2}{N}$$

#### Example
- Heights of 10 people in cm:
	- $X=\{170,165,175,160,180,172,178,169,163,177\}$
	- Estimate the parameters of the Gaussian (normal) distribution that fits this data.

##### Answer
- To find the mean $(m\  / \ \mu ):$
	- $$\sum_{t}x^{t} = total\ sum \ of \ outcomes $$
	- $$\sum_{t}x^{t}=170+165+175+160+180+172+178+169+163+177$$
	- $$\sum_{t}x^t = 1,709$$
	- $$N = Number \ of \ outcomes = 10$$
	- $$\mu = \frac{\sum_{t}x^t}{N}$$
###### - $$\mu = \frac{1709}{10} = 170.9$$
---

- To find the variance $(\sigma^{2} \ or \ s^2):$
	- $$N = Number \ of \ outcomes$$
	- $Find \ the \ value \ for \ (x^t-\mu)^2$
		- $$x_{1} ; \ (170 - 170.9)^{2}= (-0.9)^{2}= 0.81$$
		- $$x_2 ; \ (165 - 170.9)^{2}= (-5.9)^{2}= 34.81$$
		- $$x_3 ; \ (175 - 170.9)^{2}= (4.1)^{2}= 16.81$$
		- $$x_4 ; \ (160 - 170.9)^{2}= (-10.9)^{2}= 118.81$$
		- $$x_5 ; \ (180 - 170.9)^{2}= (9.1)^{2}= 82.81$$
		- $$x_6 ; \ (172 - 170.9)^{2}= (1.1)^{2}= 1.21$$
		- $$x_7 ; \ (178 - 170.9)^{2}= (7.1)^{2}= 50.41$$
		- $$x_8 ; \ (169 - 170.9)^{2}= (-1.9)^{2}= 3.61$$
		- $$x_9 ; \ (163 - 170.9)^{2}= (-7.9)^{2}= 62.41$$
		- $$x_{10} ; \ (177 - 170.9)^{2}= (6.1)^{2}= 37.21$$
	- $$\sum_{t} (x^{t}-\mu)^{2} = 0.81+34.81+16.81+118.81+82.81+1.21+50.41+3.61+62.41+37.21$$
	- $$\sum_{t} (x^{t}-\mu)^{2} = 408.9$$
	- $$\sigma^{2}= \frac{\sum_{t} (x^{t}-\mu)^{2}}{N}  = \frac{408.9}{10} = 40.89 \approx 40.9$$
---

- To find log likelihood:
	- $\sigma^{2}= 40.9$
	- $\sigma = 6.39$
	- $\mu = 170.9$
	- $N = 10$
	- $\sum_{t} (x^{t}-\mu)^{2} = 408.9$
	- $$L(\mu, \sigma|X) = -\frac{N}{2}\log(2\pi) - N\log \sigma - \frac{\sum_{t}(x^t-\mu)^2}{2\sigma^2}$$
	- $$L(\mu, \sigma|X) = -\frac{10}{2}\log(2*3.14) - 10\log 6.39 - \frac{408.9}{2*40.9}$$
	- $$L(\mu, \sigma|X) = -5\log(6.28) - 10\log 6.39 - \frac{408.9}{81.8}$$
	- $$L(\mu, \sigma|X) = (-5 *0.79) - (10*0.80) - 5$$
	- $$L(\mu, \sigma|X) = -3.95 - 8 - 5$$
	- $$L(\mu, \sigma|X) = -16.95$$
