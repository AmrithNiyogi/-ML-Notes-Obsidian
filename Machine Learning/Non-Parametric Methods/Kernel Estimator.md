- Kernel Estimator (Parzen windows)
	- $$\hat{p}(x) = \frac{1}{Nh}\sum_{t=1}^{N}\left( \frac{{x-x^{t}}}{h} \right)$$
- Kernel Function, K(u)
	- Gaussian kernel:
	- $$K(u)=\frac{1}{\sqrt{ 2\pi }}\exp\left[ -\frac{u^{2}}{2} \right]$$

![[Pasted image 20240917221141.png]]

## Example - 

- $$X={151,154,157,159,162,165,167,170,173,175,178,180}$$
	- $$X_{0} = 150,\  h= 5$$
	- estimate density at $x=160$


The **Kernel Density Estimator (KDE)** smooths the contribution of each data point over a range using a kernel function (typically a Gaussian kernel). The general formula for KDE is:

$$\hat{p}(x) = \frac{1}{Nh}\sum_{t=1}^{N}\left( \frac{{x-x^{t}}}{h} \right)$$
We shall use a Gaussian Kernel :
$$K(u)=\frac{1}{\sqrt{ 2\pi }}\exp\left[ -\frac{u^{2}}{2} \right]$$

For each point $x_{i}$ in $X$, we calculate $K\left( \frac{{x-x^{t}}}{h} \right)$ at $x = 160$ with $h=5$:

- For $x_{1} = 151$:
$$u = \frac{{160 - 151}}{5} = \frac{9}{5} = 1.8$$
$$\frac{u^{2}}{2}= \frac{1.8^{2}}{2} = \frac{3.24}{2} = 1.62$$
$$K(1.8) = \frac{1}{\sqrt{ 2\pi }}\exp[-1.62] \approx 0.0897$$
- For $x_{2} = 154$:
$$u = \frac{{160 - 154}}{5} = \frac{6}{5} = 1.2$$
$$\frac{u^{2}}{2}= \frac{1.2^{2}}{2} = \frac{1.44}{2} = 0.72$$
$$K(1.2) = \frac{1}{\sqrt{ 2\pi }}\exp[-0.72] \approx 0.1942$$
- For $x_{3} = 157$:

$$u = \frac{{160 - 157}}{5} = \frac{3}{5} = 0.6$$
$$\frac{u^{2}}{2}= \frac{0.6^{2}}{2} = \frac{0.36}{2} = 0.18$$
$$K(0.6) = \frac{1}{\sqrt{ 2\pi }}\exp[-0.18] \approx 0.3332$$
- For $x_{4} = 159$:

$$u = \frac{{160 - 159}}{5} = \frac{1}{5} = 0.2$$
$$\frac{u^{2}}{2}= \frac{0.2^{2}}{2} = \frac{0.04}{2} = 0.02$$
$$K(0.2) = \frac{1}{\sqrt{ 2\pi }}\exp[-0.02] \approx 0.3910$$
- For $x_{5} = 162$:

$$u = \frac{{160 - 162}}{5} = -\frac{2}{5} = -0.4$$
$$\frac{u^{2}}{2}= \frac{-0.4^{2}}{2} = \frac{0.16}{2} = 0.08$$
$$K(-0.4) = \frac{1}{\sqrt{ 2\pi }}\exp[-0.08] \approx 0.3683$$
- For $x_{6} = 165$:

$$u = \frac{{160 - 165}}{5} = -\frac{5}{5} = -1.0$$
$$\frac{u^{2}}{2}= \frac{-1.0^{2}}{2} = \frac{1.0}{2} = 0.5$$
$$K(-1.0) = \frac{1}{\sqrt{ 2\pi }}\exp[-0.5] \approx 0.2419$$
- For $x_{7} = 167$:

$$u = \frac{{160 - 167}}{5} = -\frac{7}{5} = -1.4$$
$$\frac{u^{2}}{2}= \frac{-1.4^{2}}{2} = \frac{1.96}{2} = 0.98$$
$$K(-1.4) = \frac{1}{\sqrt{ 2\pi }}\exp[-0.98] \approx 0.1497$$
- For $x_{8} = 170$:

$$u = \frac{{160 - 170}}{5} = -\frac{10}{5} = -2.0$$
$$\frac{u^{2}}{2}= \frac{-2.0^{2}}{2} = \frac{4.0}{2} = 2.0$$
$$K(-2.0) = \frac{1}{\sqrt{ 2\pi }}\exp[-2.0] \approx 0.0539$$
- For $x_{9} = 173$:

$$u = \frac{{160 - 173}}{5} = -\frac{13}{5} = -2.6$$
$$\frac{u^{2}}{2}= \frac{-2.6^{2}}{2} = \frac{6.76}{2} = 3.38$$
$$K(-2.6) = \frac{1}{\sqrt{ 2\pi }}\exp[-3.38] \approx 0.0177$$
- For $x_{10} = 175$:

$$u = \frac{{160 - 175}}{5} = -\frac{15}{5} = -3$$
$$\frac{u^{2}}{2}= \frac{-3.0^{2}}{2} = \frac{9.0}{2} = 4.5$$
$$K(-4.5) = \frac{1}{\sqrt{ 2\pi }}\exp[-4.5] \approx 0.0044$$
- For $x_{11} = 178$:

$$u = \frac{{160 - 178}}{5} = -\frac{18}{5} = -3.6$$
$$\frac{u^{2}}{2}= \frac{-3.6^{2}}{2} = \frac{12.96}{2} = 6.48$$
$$K(-3.6) = \frac{1}{\sqrt{ 2\pi }}\exp[6.48] \approx 0.0015$$
- For $x_{12} = 180$:

$$u = \frac{{160 - 180}}{5} = -\frac{20}{5} = -4.0$$
$$\frac{u^{2}}{2}= \frac{-4.0^{2}}{2} = \frac{16.0}{2} = 8.0$$
$$K(-4.0) = \frac{1}{\sqrt{ 2\pi }}\exp[-8.0] \approx 0.0003$$

#### Summing all the values
$$K(1.8)+K(1.2)+K(0.6)+K(0.2)+K(−0.4)+K(−1.0)+K(−1.4)+K(−2.0)+K(−2.6)+K(−3.0)+K(−3.6)+K(−4.0) $$$$=0.0897+0.1942+0.3332+0.3910+0.3683+0.2419+0.1497+0.0539+0.0177+0.0044+0.0015+0.0003$$$$≈1.8458$$
### KDE Estimate at $x = 160$

$$f(160) = \frac{1}{Nh} \sum_{i=1}^{N}K\left( \frac{{160-x_{i}}}{h} \right)$$
$$f(160) = \frac{1}{12*5}*1.8458 = \frac{1.8458}{60} \approx 0.0308$$