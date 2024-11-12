- Generalization of Lagrange's Multiplier
- Let f(x) function needs to be optimized subject to conditions:
	- $$g_{i}(x) \le 0 \ \mathrm{for} \ i=1,\dots,m \left( \mathrm{inequality \ constraints} \right)$$
	- $$g_{j}(x) = 0 \ \mathrm{for} \ j=1,\dots,p \left( \mathrm{equality \ constraints} \right)$$
- KKT Conditions:
	1. Convert optimization function to Lagrange's function and take derivative w.r.t to only those constants not-associated with inequalities.
		- $$\nabla f(x) + \sum^{m}_{i=1}\lambda_{i}\nabla g_{i}(x) + \sum^{p}_{j=1} v_{j}\nabla h_{j}(x) = 0$$
	2. Solution must satisfy original constraints:
		- $$g_{i}(x) \le 0 \ \mathrm{and} \ h_{j}(x) = 0$$
	3. For all inequalities:
		- $$\lambda_{i}g_{i}(x) = 0$$
	4. Lagrange's multipliers for all inequalities must be:
		- $$\lambda_{i} \ge 0$$

