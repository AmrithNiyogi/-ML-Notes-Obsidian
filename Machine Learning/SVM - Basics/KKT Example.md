- max function f:

$$f(x_{1},x_{2},x_{3}) = -x_{1}^{2}-x_{2}^{2}= x_{3}^{2}+4x_{1}+6x_{2}$$

- subject to constraints
	- $x_{1} + x_{2} \le 2$
	- $2x_{1} + 3x_{2} \le 12$


Solve it...

- Ans:
	- Optimal point: (1⁄2, 3/2, 0)
	- Lagrange multipliers: (3,0)
	- Optimal Value: 17/2


---
---


# Solution

Given function - 

$$f(x_{1},x_{2},x_{3}) = -x_{1}^{2}-x_{2}^{2}= x_{3}^{2}+4x_{1}+6x_{2}$$
Constraints - 
 $$x_{1} + x_{2} \le 2$$ $$2x_{1} + 3x_{2} \le 12$$
$$x_{1},x_{2},x_{3} \ge 0$$

## Step 1 - Define the Lagrangian Equation

$$L(x_{1},x_{2},x_{3},\lambda_{1},\lambda_{2}) = -x_{1}^{2}-x_{2}^{2}= x_{3}^{2}+4x_{1}+6x_{2} + \lambda_{1}(2-x_{1}-x_{2}) + \lambda_{2}(12-2x_{1}-3x_{2})$$

## Step 2 - Calculating the partial derivatives

### solving for $x_{1}$

$$\frac{\partial L}{\partial x_{1}} = -2x_{1} + 4 -\lambda_{1} - 2\lambda_{2} = 0$$
$$x_{1} = \frac{{4-\lambda_{1}-2\lambda_{2}}}{2}$$
### solving for $x_{2}$
$$\frac{\partial L}{\partial x_{2}} = -2x_{1} + 6 -\lambda_{1} - 3\lambda_{2} = 0$$
$$x_{2} = \frac{{6-\lambda_{1}-3\lambda_{2}}}{2}$$
### solving for $x_{3}$
$$\frac{\partial L}{\partial x_{2}} =2x_{3}  = 0$$
This implies $x_{3} = 0$

### slackness conditions

$$\lambda_{1}(2-x_{1}-x_{2}) = 0$$
$$\lambda_{2}(12-2x_{1}-3x_{2}) = 0$$

## solving the cases

### case 1 - $\lambda_{1}=0, \lambda_{2}=0$
1. $$x_{1} = \frac{{4-0-0}}{2} = 2$$
2. $$x_{2} = \frac{{6-0-0}}{2} = 3$$
$$x_{1}+x_{2} = 2+3 = 5 \not\le 2$$

### case 2 - $\lambda_{1} \ne0, \lambda_{2}=0$

$$x_{1} + x_{2} = 2 \Rightarrow x_{2} = 2 - x_{1}$$
$$2x_{1}+3x_{2} \le 12$$
$$2x_{1}+ 3(2-x_{1}) = 2x_{1} - 3x_{1} + 6 = -x_{1} + 6$$
$$-x_{1}+6 \le 12 \Rightarrow x_{1} \ge -6$$
### case 3 - $\lambda_{1}=0, \lambda_{2}\neq0$


### case 4 - $\lambda_{1}\ne0, \lambda_{2}\ne0$





---

- From first constraint being active (since $\lambda_1 \neq 0$): $$x_1 + x_2 = 2$$
- We have: $$x_1 = \frac{4-\lambda_1}{2}$$ $$x_2 = \frac{6-\lambda_1}{2}$$
- Substituting these into constraint: $$\frac{4-\lambda_1}{2} + \frac{6-\lambda_1}{2} = 2$$ $$10-2\lambda_1 = 4$$ $$-2\lambda_1 = -6$$ $$\lambda_1 = 3$$
- Therefore: $$x_1 = \frac{4-3}{2} = \frac{1}{2}$$ $$x_2 = \frac{6-3}{2} = \frac{3}{2}$$
- Check second constraint: $$2(\frac{1}{2}) + 3(\frac{3}{2}) = 1 + \frac{9}{2} = \frac{11}{2} < 12$$ (satisfied)

### Case 3 - $\lambda_1 = 0, \lambda_2 \neq 0$

1. From second constraint being active: $$2x_1 + 3x_2 = 12$$
2. We have: $$x_1 = \frac{4-2\lambda_2}{2} = 2-\lambda_2$$ $$x_2 = \frac{6-3\lambda_2}{2} = 3-\frac{3\lambda_2}{2}$$
3. Substituting into active constraint: $$2(2-\lambda_2) + 3(3-\frac{3\lambda_2}{2}) = 12$$ $$4-2\lambda_2 + 9-\frac{9\lambda_2}{2} = 12$$ $$13-2\lambda_2-\frac{9\lambda_2}{2} = 12$$ $$13-\frac{13\lambda_2}{2} = 12$$ $$-\frac{13\lambda_2}{2} = -1$$ $$\lambda_2 = \frac{2}{13}$$
4. Therefore: $$x_1 = 2-\frac{2}{13} = \frac{24}{13}$$ $$x_2 = 3-\frac{3}{13} = \frac{36}{13}$$
5. Check first constraint: $$\frac{24}{13} + \frac{36}{13} = \frac{60}{13} > 2$$ (not satisfied)

### Case 4 - $\lambda_1 \neq 0, \lambda_2 \neq 0$

1. Both constraints active: $$x_1 + x_2 = 2$$ $$2x_1 + 3x_2 = 12$$
2. From first equation: $$x_1 = 2-x_2$$
3. Substitute into second: $$2(2-x_2) + 3x_2 = 12$$ $$4-2x_2 + 3x_2 = 12$$ $$4 + x_2 = 12$$ $$x_2 = \frac{3}{2}$$
4. Therefore: $$x_1 = 2-\frac{3}{2} = \frac{1}{2}$$
5. Find Lagrange multipliers from: $$-2x_1 + 4 - \lambda_1 - 2\lambda_2 = 0$$ $$-2x_2 + 6 - \lambda_1 - 3\lambda_2 = 0$$ Substituting $x_1=\frac{1}{2}, x_2=\frac{3}{2}$: $$-2(\frac{1}{2}) + 4 - \lambda_1 - 2\lambda_2 = 0$$ $$-2(\frac{3}{2}) + 6 - \lambda_1 - 3\lambda_2 = 0$$ $$3 = \lambda_1 + 2\lambda_2$$ $$3 = \lambda_1 + 3\lambda_2$$ Solving: $$\lambda_2 = 0$$ $$\lambda_1 = 3$$
6. Optimal value: $$f(\frac{1}{2}, \frac{3}{2}, 0) = -(\frac{1}{2})^2 - (\frac{3}{2})^2 - 0^2 + 4(\frac{1}{2}) + 6(\frac{3}{2})$$ $$= -\frac{1}{4} - \frac{9}{4} + 2 + 9$$ $$= -\frac{10}{4} + 11$$ $$= \frac{17}{2}$$

Case 4 gives us the optimal solution since:

- It satisfies all constraints
- The Lagrange multipliers are non-negative
- The objective value is maximum among all feasible cases

Therefore:

- Optimal point: $(1/2, 3/2, 0)$
- Lagrange multipliers: $(3,0)$
- Optimal value: $17/2$