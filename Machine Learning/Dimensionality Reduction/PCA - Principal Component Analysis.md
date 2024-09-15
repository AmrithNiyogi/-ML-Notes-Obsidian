- Find a low-dimensional space (from d to k, k < d) such that when x is projected there, information loss is minimum.
- The projection of x on the direction of w is - $z = w^{T}x$
- Unsupervised technique
- Find w such that Var(z) is maximum


- For a Unique solution and to make direction important factor $||w|| = 1$
	- $Var(z) = Var(w^{T}x) = E[(w^{T}x - w^{T}\mu)^2]$
	- $Var(z) = E[(w^{T}x - w^{T}\mu)(w^{T}x - w^{T}\mu)]$
	- $Var(z) = E[w^T(x-\mu)(x-\mu)^{T}w]$
	- $Var(z) = w^{T}E[(x-\mu)(x-\mu)^{T}]w = w^{T}\sum w$
	- $Cov(x) =\sum$



- Maximize Var(z) subject to $||w|| = 1$ i.e., $w_{1}^{T}w_{1} = 1$
	- $$max_{w_{1}} w_{1}^{T}\sum w_{1} - \alpha (w_{1}^{T}w_{1} - 1) $$
	- $\sum w_{1} = aw_{1}$ that is, $w_{1}$ is an eigenvector of $\sum$ , with the largest eigenvalue $a$
		- $$w_{1}^{T}\sum w_{1} = \alpha w_{1}^{T}w_{1} = \alpha$$
- Second PC, $w_2$ should also maximize Var($z_2$), be of unit 1 and orthogonal to $w_1$
	- $$max_{w_{2}} w_{2}^{T}\sum w_{2} - \alpha(w_{2}^{T}w_{2}-1) - \beta(w_{2}^{T}w_{1}-0)$$
	- $\sum w_{2} = \alpha w_{2}$ that is $w_{2}$ is another eigenvector of $\sum$
- so on for other dimensions...



- Let dataset with 2 features and 3 data points -
	- $$\Bigg[\begin{matrix}
1 \ \ \ 2 \\ 
2 \ \ \ 3  \\
3 \ \ \ 4
\end{matrix}\Biggr]$$
1. Calculate Covariance Matrix 
	- $$\sum = \frac{1}{(n-1)}X^T_{centered}X_{centered}$$
	- $$Mean = \Biggl [\begin{matrix}
\frac{1+2+3}{3} \\
\frac{2+3+4}{3}
\end{matrix}\Biggr] = \Biggl[ \begin{matrix}
2 \\
3
\end{matrix} \Biggr]$$
	- $$X_{centered} = X - Mean = \Bigg[\begin{matrix}
1 \ \ \ 2 \\ 
2 \ \ \ 3  \\
3 \ \ \ 4
\end{matrix}\Biggr] - \biggl[ \begin{matrix}
2 \ \ \ \ 3 
\end{matrix}\biggr] = \Bigg[\begin{matrix}
-1 \ \ \ -1 \\ 
0 \ \ \ 0  \\
1 \ \ \ 1
\end{matrix}\Biggr] $$
	- $$\sum = \frac{1}{2}\Bigg[\begin{matrix}
-1 \ \ \ -1 \\ 
0 \ \ \ 0  \\
1 \ \ \ 1
\end{matrix}\Biggr] \Bigg[\begin{matrix}
-1 \ \ \ 0  \ \ \ -1\\ 
-1 \ \ \ 0  \ \ \ -1\\
\end{matrix}\Biggr] = \Bigg[\begin{matrix}
1 \ \ \ 1 \\ 
1 \ \ \ 1
\end{matrix}\Biggr] $$

2. Find eigenvalues and eigenvectors
	- $\det\left( \sum - \lambda I \right) = 0$;    Eigenvalues: $\lambda_{1} = 2, \ \lambda_{2} = 0$
	- $For \ \lambda_{1} = 2$
		- $$\bigg[\begin{matrix}
(1-2) \ \ \ \ \ \  1 \\
1 \ \ \ \ \ \  (1-2)
\end{matrix}\bigg]  \bigg[\begin{matrix}
v_{1}  \\
v_{2}
\end{matrix}\bigg] = \bigg[\begin{matrix}
0\\
0
\end{matrix}\bigg]$$
		- Solving this we get:
			- $$v_{1} = \bigg[ \begin{matrix}
1 \\
1
\end{matrix}\bigg]$$
	- $For \ \lambda_{2} = 0$
	- $$\bigg[\begin{matrix}
(1-2) \ \ \ \ \ \  1 \\
1 \ \ \ \ \ \  (1-2)
\end{matrix}\bigg]  \bigg[\begin{matrix}
v_{1}  \\
v_{2}
\end{matrix}\bigg] = \bigg[\begin{matrix}
0\\
0
\end{matrix}\bigg]$$
		- Solving this we get:
			- $$v_{1} = \bigg[ \begin{matrix}
1 \\
1
\end{matrix}\bigg]$$
3. Normalize the eigenvector corresponding to the largest eigenvalue $\lambda_{1}$
	- $$v_{1} = \frac{1}{\sqrt{ 2 }} \biggl[ \begin{matrix}
1 \\
1
\end{matrix}\biggr] = \biggl[ \begin{matrix}
0.707 \\
0.707
\end{matrix}\biggr] $$

4. Projection of centered data onto the eigenvector $v_{1}$
	- $z = X_{centered}v_{1}$
	- $$\Bigg[\begin{matrix}
-1 \ \ \ -1 \\ 
0 \ \ \ 0  \\
1 \ \ \ 1
\end{matrix}\Biggr] 
\bigg[\begin{matrix}
0.707 \\
0.707
\end{matrix}\bigg]
= \Bigg[ \begin{matrix}
-1.414 \\
0 \\
-1.414
\end{matrix}\Bigg]$$


- k Eigenvectors with non-zero eigenvalues are the dimensions of the reduced space
- The first eigenvector(the one with the largest eigenvalue, $w_1$, explains the largest part of the variance; the second explains the second largest; and so on)
- PCA centers the data and rotates the axes to line up with the directions of the highest variances


![[Pasted image 20240814114524.png]]
