

- How many training examples N should we have, such that with probability at least 1 - $\delta$, h as error at most $\epsilon$ for arbitrary $\delta$ <= 1/2 and Ē > 0 
- Each strip is at most $\epsilon$/4
- Probability that we miss a strop 1 - $\epsilon$/4
- Probability that *N* instances miss a strip (1 - $\epsilon$/4)^N
- Probability that *N* instances miss 4 strips is at most 4(1 - $\epsilon$/4)^N
- 4(1 - $\epsilon$/4)^N <= $\delta$ and (1-x)<= exp(-x)
- 4exp(-$\epsilon$N/4) <= $\delta$ and N >= (4/$\epsilon$)log(4/$\delta$)
	- that is, we take at least (4/$\epsilon$)log(4/$\delta$) independent examples from C




![[Pasted image 20240723220407.png]]
