- Boolean function XOR as disjunction of conjunctions:
$$x_{1} \ \mathrm{XOR} \ x_{2} = (x_{1} \ \mathrm{AND} \sim x_{2}) \ \mathrm{OR} \ (\sim x_{1} \ \mathrm{AND} \ x_{2})$$
- Each conjunction is implemented by one hidden layer
- Disjunction is implemented by output layer
- 2 perceptrons implement two ANDs in parallel and another perceptron on top OR them
- Both inputs, $(0,0)$ and $(1,1)$, are mapped to $(0,0)$ in the $(z_{1},z_{2})$ space, allows linear separability in this second space


![[Pasted image 20241112114515.png]]


| $x_{1}$ | $x_{2}$ | $y$ |
| ------- | ------- | --- |
| 0       | 0       | 0   |
| 0       | 1       | 1   |
| 1       | 0       | 1   |
| 1       | 1       | 0   |

| $z_{1}$ | $z_{2}$ | $y$ |
| ------- | ------- | --- |
| 0       | 0       | 0   |
| 0       | 1       | 1   |
| 1       | 0       | 1   |
| 0       | 0       | 0   |