- Two outcomes - success/occurs and failures/not-occurs {1,0}
- Event is occurred, X = 1 with probability p:
- Non-occurrence of event, X=0, probability = 1-p
	- $$P(x) = p^{x}(1-p)^{1-x}, x \in \lbrace 0, 1 \rbrace $$
- Log Likelihood:
	- $$L(p|X) = \log \prod^N_{t=1}p^{(x^{t)}}(1-p)^{(1-x^t)}$$
	- $$ = \sum_{t}x^{t}\log p + \left( N - \sum_{t}x^t \right) \ \log(1-p) $$
- MLE:
	- $$\hat{p} = \frac{\sum_{t}x^{t}}{N}$$

<h4>Example</h4>
- Biased Coin Flip - 10 times
	- H = 1
	- T = 0
	- $X = \{1,0,1,1,0,1,0,1,1,0\}$
- Estimate the probability of getting heads (success) using MLE.

- $p= number \ of \ heads = 6$
- $(1-{p}) = number \ of \ tails = 4$
- $\sum_{t}x^{t} = 1 + 1 + 1 + 1 + 1 + 1 = 6$
- $\sum_{t}y^{t} = 1 + 1 + 1 + 1 = 4$
- $N = total \ number \ of \ outcomes = {p} + (1-{p}) = 6 + 4 = 10$

Therefore,

$$ The \ probability \ of \ getting \ heads = \hat{p} = \frac{\sum_{t}x^t}{N}$$
$$ \hat{p} = \frac{6}{10} = 0.6$$
similarly,
$$ The \ probability \ of \ getting \ tails = (1-\hat{p}) = \frac{\sum_{t}y^t}{N}$$
$$ \hat{p} = \frac{4}{10} = 0.4$$