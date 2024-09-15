- Credit Scoring:
	- Inputs:
		- income, $x_{1}$ and savings $x_2$
	- Output:
		- low-risk vs high-risk
- Input: $x = [x_{1}, x_{2}]$ T, Output: $C \varepsilon \lbrace 0, 1 \rbrace$
- Prediction:
	- $$ choose \Biggl\lbrace 
	 \begin{matrix} \
 C = 1 \ if\ P(C=1|x_{1}x_{2}) > 0.5\\ \\
C = 0 \ othewise
\end{matrix} $$
	- or
	- $$ choose \Biggl\lbrace 
	 \begin{matrix} \
 C = 1 \ if\ P(C=1|x_{1}x_{2}) > P(C=0 | x_{1}x_{2})\\ \\
C = 0 \ othewise
\end{matrix} $$

