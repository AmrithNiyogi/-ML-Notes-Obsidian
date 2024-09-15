$$P(C_{i}|x) = \frac{p(x|C_{i})P(C_{i})}{p(x)} = \frac{p(x|C_{i})P(C_{i})}{\sum_{k=1}^{K}p(x|C_{k})P(C_{k})}$$
- Let discriminant function:
	- $g_{i}(x) = p(x|C_{i})P(C_{i})$
	- $g_{i}(x) = \log p(x|C_{i}) + \log P(C_{i})$
- Assume $p(x|C_i)$ are Gaussian
	- $$p(x|C_{i}) = \frac{1}{\sqrt{ 2\pi }\sigma_{i}} \exp \Biggl[ - \frac{( x-\mu_{i}^{2})}{2\sigma^2_{i}} \Biggr]$$
	- $$g_{i}(x) = -\frac{1}{2}\log{2\pi} -\log \sigma_{i} -\frac{(x-\mu_{i})^2}{2\sigma^2_{i}} +\log P(C_{i})$$
- Let the sample:
	- $$X = \lbrace x^t,r^t \rbrace_{t=1}^N  $$
	- $$r_{i}^{t}= \Biggl\lbrace  \begin{matrix} 
1 \ if \ x^{t} \in \ C_{j} \\
0 \ if \ x^{t} \in \ C_{j}, \imath \ne \jmath
\end{matrix}$$
- Sample Mean and Variance for Gaussian:
	- $$m_{i}=\frac{\sum_{t}x^tr^t_{i}}{\sum_{t}r^t_{i}}$$
	- $$s^{2}_{{i}}=\frac{\sum_{t}(x^{t}-m_{i})^{2}r^t_{i}}{\sum_{t}r^t_{i}}$$
- Prior Probability:
	- $$\hat{P}(C_{i}) = \frac{\sum_{t}r^t_{i}}{N}$$
- Discriminant function:
	- $$g_{i}(x) = -\frac{1}{2}\log(2\pi) -\log s_{i} - \frac{(x-m_{i})^2}{2s_{i}^2} + \log \hat{P}(C_{i})$$
	- $$g_{i}(x) = -(x-m_{i})^2$$
	- $$Choose \ C_{i} \ if \ |x-m_{i}| = min_{k} |x-m_{k}|$$
