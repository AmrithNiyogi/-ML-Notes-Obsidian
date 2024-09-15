- For the single input linear model
	- $$g(x) = w_{1}x + w_{0}$$
- $w_{1}$ and $w_{0}$ should minimise
	- $$E(w_{1}, w_{0} | X) = \frac{1}{N} \sum_{t=1}^{N}[r^{t}- (w_{1}x^{t}+ w_{0})]^2$$
- <span style="color:rgb(85, 190, 183)">Interpolation</span>: process of estimating unknown values with in the range of know training data.
- <span style="color:rgb(85, 190, 183)">Extrapolation</span>: model makes predictions outside the range of the training data.
	- e.g. predict future values but have data till present.

- $w_{1}$ and $w_{0}$ should minimize, Cost/Error
	- $$E(w_{1}, w_{0} | X) = \frac{1}{N} \sum_{t=1}^{N}[r^{t}- (w_{1}x^{t}+ w_{0})]^2$$
- Minimum values of weights is calculated by taking partial derivatives of E with respect to $w_{1}$ and $w_{0}$, set these to 0 and solve
	- $$
	w_{1} = \frac{\sum_{t}x^{t}{r^{t}-}\bar{xr}N}{\sum_{t}(x^{t)^{2}}-N\bar{x}^{2}}
	$$$$
	w<span style="color:rgb(255, 0, 0)">_{0} = \bar{r} - w_{1}\bar{x}
$$
$$
\bar{x} = {\sum_{t}\frac{x^t}{N}}
$$
			and
			$$
			\bar{r} = {\sum_{t}\frac{r^t}{N}}
$$


---
To minimize $w_{1}$ and $w_{0}$, taking partial derivative with respect to $w_{0}$ 
$$
\frac{\partial E}{\partial w_{0}} = \frac{2}{N} \sum_{t=1}^{N}[r^{t} - (w_{1}x^{t}+w_{0})]
$$


Equating to 0,
$$
\frac{-2}{N} \sum_{t}[r^t-w_{1}x^t-w_{0}](1)= 0
$$
$$\sum_{t}[r^t-w_{1}x^t-w_{0}]= 0$$$$
\sum_{t=1}^{N}w_{0} + \sum_{t=1}^{N}w_{1}x^{t} = \sum_{t=1}^{N}r^{t}\to 1
$$
Now taking partial derivative with respect to $w_{1}$
$$
\frac{\partial E}{\partial w_{1}} = \frac{1}{N} \sum^{N}_{t=1}(r^{t}- (w_{1}x^t))*2[-x^t]
$$
$$
= \frac{-2}{N} \sum^{N}_{t=1}[r^{t}- (w_{1}x^{t}+ w_{0})]x^t
$$
Equating to 0
$$\frac{-2}{N} \sum_{t}[r^t-w_{1}x^t-w_{0}]x^t= 0$$
$$
\frac{-2}{N} \sum_{t}[r^t-w_{1}x^t-w_{0}]= 0
$$
$$\sum_{t}[r^tx^t-w_{1}(x^t)^2-w_{0}x_{t}]= 0$$
$$
\sum_{t=1}^{N}w_{0}x^{t} + \sum_{t=1}^{N}w_{1}(x^{t})^2 = \sum_{t=1}^{N}r^{t}x^t\to 2
$$
$$
\begin{equation}
\begin{pmatrix} 
N \  \sum_{t=1}^{Nx^{t}} \\
\sum_{t=1}^Nx^{t} \ \sum_{t=1}^N({x^{t}})^2
\end{pmatrix}
\begin{pmatrix} 
w_{0} \\
w_{1}\\

\end{pmatrix}
=
\begin{pmatrix}
\sum_{t=1}^N r^t \\
\sum_{t=1}^{N}r^tx^t
\end{pmatrix}
\end{equation}
$$
$$
w_{0}N + w_{1}\sum^{N_{t=1} x^{t}} = \sum^{N_{t=1}}r^{t}\to 3
$$
$$
w_{0}\sum^{N_{t=1}x^{t}+}w_{1} \sum^{N}_{t=1}(x^{t)^{2}} = \sum^{N_{t=1}}r^{tx^{t}}\to 4 
 $$
 from $equation - 3$
 $$
 w_{0} = \sum_{t=1}^{N}r^{t} - w_{1}\sum_{t=1}^{N}x^t
$$
$$
w_{0} = \bar{r} - w_{1}\bar{x}
$$

$$
(\bar{r} - w_{1}\bar{x}) \sum_{t=1}^{N}x^{t}+ w_{1} \sum_{t=1}^{N}(x^{t)^{2}} = \sum_{t=1}^{N}x^tr^t
$$
$$
\bar{r}\sum_{t=1}^{N}x^{t} - w_{1}\bar{x}\sum_{t=1}^{N}x^{t} +  w_{1} \sum_{t=1}^{N}(x^{t)^{2}} = \sum_{t=1}^{N}x^tr^t
$$
$$
w_{1} \left[ \sum_{t=1}^{N}(x^{t)^{2}}- \bar{x} \sum_{t=1}^{N}x^{t} \right] = \sum_{t=1}^{N}x^{tr^{t}=}\bar{r}\sum_{t=1}^{N}x^t
$$
$$
w_{1} = \frac{\sum_{t=1}^{N}x^{t}r^{t} - \bar{r} \sum_{t=1}^{N}x^t}{\sum_{t=1}^{N}(x^{t)^{2}}-\bar{x} \sum_{t=1}^{N}x^{t}}
$$

Divide numerator and denominator by N

$$
w_{1} = \frac{\frac{\sum_{t=1}^{N}x^{t}r^{t}}{N} - \frac{\bar{r} \sum_{t=1}^{N}x^t}{N}}{\frac{\sum_{t=1}^{N}(x^{t)^{2}}}{N} - \frac{\bar{x} \sum_{t=1}^{N}x^{t}}{N}}
$$

$$
w_{1} = \frac{{\frac{\sum{x^{t}r^{t}}}{N}} - {\bar{r}\bar{x}}}{\frac{\sum(x^{t})^{2}}{N} - {\bar{x}^{2}}} = \frac{Covariance(X,Y)}{Variance(X)} = \frac{\sum_{t=1}^{N}x^{t}r^{t}- \bar{x}\bar{r}N}{\sum_{t=1}^{N}(x^{t)^{2}}- \bar{x}^{2}N}
$$


$$
w_{0} = \bar{r} - \frac{Covariance(x,r)}{Variance(x)} \bar{x}
$$

$$
g(x) = w_{0} + w_{1}x
$$
$$
y = mx + c
$$
$$
g(x) = \bar{r} - \frac{\frac{Cov}{x_{1}r}}{Var(r)} \bar{x} + \frac{Cov(x_{1}r)}{Var(x)}x
$$
$$
g_{x} = \bar{r}t + \frac{Cov(x,r)}{Var(x)}[x.\bar{x}]
$$
1. $\bar{r}t \to Intercept$
2. $Var(x) \to slope$



- This is where covariance and variance come in:
	- The numerator, $\sum X_{i} Y_{i} - n \bar{X} \bar{Y}$, is n times the sample covariance of X and Y.
	- The denominator, $\sum X_{i}^{2} - n \bar{X}^2$ 
- So we can rewrite $w_{1}$ as:
	- $w_{1} = \frac{Cov(X,Y)}{Var(X)}$
- This clearly shows how the slope of the regression line is directly related to the covariance of X and Y, and inversely related to the variance of X.



- Example: 
	- Data:
		- In a chemical reaction, mass, y (grams), of a chemical is related to the time, x (seconds)
		• Equation of the regression line ?

| **Time** | *x(seconds)*   | 5   | 7   | 12  | 16  | 20  |
| -------- | -------------- | --- | --- | --- | --- | --- |
| **Mass** | ***y(grams)*** | **40**  | **120** | **180** | **210** | **240** |
![[Pasted image 20240802112221.png]]

#### Solution: 	

To find the regression line, we need to find $w_{0}$ and $w_{1}$:

$y = w_{0} + w_{1}x$

$w_{0} = \bar{y} - w_{1} \bar{x}$

$$w_{1} = \frac{\frac{\sum y_{i}x_{i}}{N} - \bar{y}\bar{x}}{\frac{\sum x_{i}^2}{N} - \bar{x}^2}$$
$$
\bar{x} = \frac{\sum x}{N} = \frac{5 +7 + 12 + 16 + 20}{5} = \frac{60}{5} = 12
$$
$$
\bar{y} = \frac{\sum y}{N} = \frac{40 + 120 + 180 + 210 + 240}{5} = \frac{790}{5} = 158
$$
$\bar{x}\bar{y} = 12 * 158 = 1896$

| $x_{i}$ | $y_{i}$ | $y_{i}x_{i}$ | $x_{i}^2$ |
| ------- | ------- | ------------ | --------- |
| 5       | 40      | 200          | 25        |
| 7       | 120     | 840          | 49        |
| 12      | 180     | 2160         | 144       |
| 16      | 210     | 3360         | 256       |
| 20      | 240     | 4800         | 400       
$\sum y_{i}x_{i} = 11360$
$\sum x_{i}^{2}= 874$

putting these values in $w_{1}$:

$$
w_{1} = \frac{\frac{11360}{5}- 1896}{\frac{874}{5}-144}
$$
$$
 w_{1 }= \frac{37.6}{30.8} = 12.208
$$
$$
\begin{matrix}
w_{0} = 158 - (12*12.208) \\
w_{0} = 158 - 146.494 \\
w_{0} = 11.506 
\end{matrix}
$$
