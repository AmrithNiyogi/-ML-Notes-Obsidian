- $$P(C_{i}|x) = \frac{{p(x|C_{i})P(C_{i})}}{p(x)}$$
- $$P(C_{i}|x) = \frac{{p(x|C_{i})P(C_{i})}}{\sum_{k=1}^{K}p(x|C_{k})P(C_{k})}$$
- $P(C_{i}) \ge0$ and $\sum_{k=1}^{K}P(C_{i})=1$
- choose $C_{i}$ if $P(C_{i}|x) = max_{k} P(C_{k}|x)$


<h3> Example </h3>
<table>
	<tr>
		<th>Outlook</th>
		<th>Temp</th>
		<th>Humidity</th>
		<th>Windy</th>
		<th>Play Golf</th></tr>
	<tr>
		<th>Rainy</th>
		<th>Hot</th>
		<th>High</th>
		<th>False</th>
		<th>No</th></tr>
	<tr>
		<th>Rainy</th>
		<th>Hot</th>
		<th>High</th>
		<th>True</th>
		<th>No</th></tr>
	<tr>
		<th>Overcast</th>
		<th>Hot</th>
		<th>High</th>
		<th>False</th>
		<th>Yes</th></tr>
	<tr>
		<th>Sunny</th>
		<th>Mild</th>
		<th>High</th>
		<th>False</th>
		<th>Yes</th></tr>
	<tr>
		<th>Sunny</th>
		<th>Cool</th>
		<th>Normal</th>
		<th>False</th>
		<th>Yes</th></tr>
	<tr>
		<th>Sunny</th>
		<th>Cool</th>
		<th>Normal</th>
		<th>True</th>
		<th>No</th></tr>
	<tr>
		<th>Overcast</th>
		<th>Cool</th>
		<th>Normal</th>
		<th>True</th>
		<th>Yes</th></tr>
	<tr>
		<th>Rainy</th>
		<th>Mild</th>
		<th>High</th>
		<th>False</th>
		<th>No</th></tr>
	<tr>
		<th>Rainy</th>
		<th>Cool</th>
		<th>Normal</th>
		<th>False</th>
		<th>Yes</th></tr>
	<tr>
		<th>Sunny</th>
		<th>Mild</th>
		<th>Normal</th>
		<th>False</th>
		<th>Yes</th></tr>
	<tr>
		<th>Rainy</th>
		<th>Mild</th>
		<th>Normal</th>
		<th>True</th>
		<th>Yes</th></tr>
	<tr>
		<th>Overcast</th>
		<th>Mild</th>
		<th>High</th>
		<th>True</th>
		<th>Yes</th></tr>
	<tr>
		<th>Overcast</th>
		<th>Hot</th>
		<th>Normal</th>
		<th>False</th>
		<th>Yes</th></tr>
	<tr>
		<th>Sunny</th>
		<th>Mild</th>
		<th>High</th>
		<th>True</th>
		<th>No</th></tr></table>


- Weather Dataset:
- Predict: one can play golf on days with following weather conditions?
	- Today, $x_{1}$: (Sunny, Hot, Normal, False) or (S,H,N,F)
	- Future, $x_{2}$: (Rainy, Cool, High, True) (R, C, H, T)
- To find:
	- $P(Yes | x) \ \ and\ \  P(No | x)$
- To predict for $x_{1}$:
	- $$P(Yes|x_{1}) = \frac{[P(Yes)*P(s_{1}|Yes)]}{P(x_{1})}$$
	- $$P(No|x_{1}) = \frac{[P(No)*P(s_{1}|No)]}{P(x_{1})}$$

#### Answer

- $P(Yes) = \frac{9}{14}$
- $P(No) = \frac{5}{14}$

1. $P(x_{1}|Yes) = P({Sunny,Hot,Normal,False} \ | \ Yes)$
   $= P(S|Yes) * P(H|Yes) * P(N|Y) * P(F|Y)$
   $= \frac{3}{9} * \frac{2}{9} * \frac{6}{9} * \frac{6}{9}$
   $= \frac{216}{6561}$
2. $P(x_{1}|No) = P(S, H, N, F \ | \ Yes)$
   $=  P(S|No) * P(H|No) * P(N|No) * P(F|No)$
   $= \frac{2}{5} * \frac{2}{5} * \frac{1}{5} * \frac{2}{5}$
   $= \frac{8}{625}$
3. $P(Yes | x_{1} = \frac{[P(Yes) * P(x_{1} | Yes)]}{P(x_{1})})$
   $= \frac{\frac{9}{14} * \frac{216}{6561}}{P(x_{1})}$
   $= \frac{0.021}{P(x_{1})} \sim 0.021$
4.  $P(No | x_{1} = \frac{[P(No) * P(x_{1} | No)]}{P(x_{1})})$
    $= \frac{\frac{5}{14} * \frac{8}{625}}{P(x_{1})}$
    $= \frac{0.004}{P(x_{1})} \sim 0.004$
5. Normalize the probabilities:
	- $$P(Yes|x_{1})= \frac{0.021}{(0.021+0.004)} = 0.84$$
	- $$P(No|x_{1}) = \frac{0.004}{0.021+0.004} = 0.16$$

- To predict for $x_{2}$:
	- $$P(Yes|x_{2}) = \frac{[P(Yes)*P(s_{2}|Yes)]}{P(x_{2})}$$
	-  $$P(No|x_{2}) = \frac{[P(No)*P(s_{2}|No)]}{P(x_{2})}$$
<h4>Answer</h4>
- $P(Yes) = \frac{9}{14}$
- $P(No) = \frac{5}{14}$

1. $P(x_{2}|Yes) = P({Rainy,Cool,High,True} \ | \ Yes)$
   $= P(R|Yes) * P(C|Yes) * P(H|Yes) * P(T|Yes)$
   $= \frac{2}{9} * \frac{2}{9} * \frac{3}{9} * \frac{3}{9}$
   $= \frac{36}{6561}$
2. $P(x_{2}|No) = P({Rainy,Cool,High,True} \ | \ No)$
   $= P(R|N) * P(C|N) * P(H|N) * P(T|N)$
   $= \frac{3}{5} * \frac{2}{5} * \frac{4}{5} * \frac{3}{5}$
   $= \frac{72}{625}$
3. $P(Yes | x_{2} = \frac{[P(Yes) * P(x_{2} | Yes)]}{P(x_{2})})$
   $= \frac{\frac{9}{14} * \frac{36}{6561}}{P(x_{1})}$
   $= \frac{0.003}{P(x_{1})} \sim 0.003$
4.  $P(No | x_{1} = \frac{[P(No) * P(x_{1} | No)]}{P(x_{1})})$
    $= \frac{\frac{5}{14} * \frac{72}{625}}{P(x_{1})}$
    $= \frac{0.041}{P(x_{1})} \sim 0.041$
5. Normalize the probabilities:
	- $$P(Yes|x_{2})= \frac{0.003}{(0.003+0.041)} = 0.68$$
	- $$P(No|x_{2}) = \frac{0.041}{0.003+0.041} = 0.93$$
