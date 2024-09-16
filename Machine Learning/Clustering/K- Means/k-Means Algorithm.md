Initialize $m_{i}, i = 1,\dots, k$ , for example, to $k \ \mathrm{random} \ x^t$
Repeat
	For all $x^{t}\epsilon X$
		$$b^{t}_{i} \gets \Biggl\{\begin{matrix}
1 \ \mathrm{if} \ ||x^{t-m_{i}||}= min_{j} ||x^t-m_{j}|| \\
0 \ \ \ otherwise
\end{matrix}$$
	For all $m_{i}, i=1,\dots,k$
		$$m_{i} \gets \sum_{t} \frac{b^{t}_{i}x^{t}}{\sum_{t}b^{t}_{i}}$$
	 Until $m_{i}$ converge
	 