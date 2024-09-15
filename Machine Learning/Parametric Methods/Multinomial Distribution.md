- K mutually exclusive and exhaustive events
- $\sum_{p} = 1$
	- $$$P(x_{1}, x_{2}, \dots, x_{k}) = \prod^K_{i=1}p_{i}^{x_{i}}$$
-  For $X = \{x^t\}_{t=1}^N$:
	- $$\sum_{i}x^{t_{i}}= 1$$
	- $$x_{i}^{t}= \biggl\{ \begin{matrix}
1 \ if \ experiment \ t \ chooses \ state \ i \\ 
0 \ otherwise
\end{matrix}$$
- MLE:
	- $$\hat{p_{i}} = \frac{\sum_{i}x^{t_{i}}}{N}$$

#### Example
- A die is rolled 50 times:
	- Face 1: 8 times
	- Face 2: 6 times
	- Face 3: 7 times
	- Face 4: 10 times
	- Face 5: 9 times
	- Face 6: 10 times
- Estimate probability of each class

##### Answer
$$Total \ number \ of \ rolls = 50$$
$$probability(class_{i}) = \frac{(number \ of \ outcomes)_{i}}{Total \ number \ of \ rolls}$$

- $class_{1}$ - rolled a 1
- $class_{2}$ - rolled a 2
- $class_{3}$ - rolled a 3
- $class_{4}$ - rolled a 4
- $class_{5}$ - rolled a 5
- $class_{6}$ - rolled a 6

1. $$probability(class_{1}) = \frac{8}{50} = 0.16$$
2. $$probability(class_{2}) = \frac{6}{50} = 0.12$$
3. $$probability(class_{3}) = \frac{7}{50} = 0.14$$
4. $$probability(class_{4}) = \frac{10}{50} = 0.20$$
5. $$probability(class_{5}) = \frac{9}{50} = 0.18$$
6. $$probability(class_{6}) = \frac{10}{50} = 0.20$$

