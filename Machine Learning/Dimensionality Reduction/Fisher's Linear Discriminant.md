- Find w that maximises:
	- $$J (w) = \frac{(m_{1} - m_{2})^2}{s^{2}_{1} + s^{2}_{2}}$$
- Between class scatter matrix:
	- $$(m_{1} - m_{2})^{2}= (w^{T}m_{1}- w^{T}m_{2})^2$$
	- $$(m_{1} - m_{2})^{2}= w^{T}(m_{1} - m_{2})(m_{1}- m_{2})^{T}w$$
	- $$(m_{1} - m_{2})^{2}= w^{T}S_{0}w$$ where $S_{0} = (m_{1} - m_{2})(m_{1}- m_{2})^{T}$ 
- With-in class matrix:
	- $$s^{2}_{1}= \sum(w^{t}x^{t}-m_{1})^{2}r^{t}$$
	- $$s^{2}_{1} = \sum w^{t}(x^{t}- m_{1})(x^{t}-m_{1})^{T}wr^{t} = w^{t}S_{1}w$$
	- where $S_{1} = (x^{t}- m_{1})(x^{t}-m_{1})^{T}r^t$

	- $$s^{2}_{2}= \sum(w^{t}x^{t}-m_{2})^{2}r^{t}$$
	- $$s^{2}_{2} = \sum w^{t}(x^{t}- m_{2})(x^{t}-m_{2})^{T}wr^{t} = w^{t}S_{2}w$$
	- where $S_{2} = (x^{t}- m_{2})(x^{t}-m_{2})^{T}r^t$

	- $s_{1}^{2}+s_{2}^{2}= w^{t}S_{w}w$ where $S_{w} = s_{1} + s_{2}$

- Find $w$ that maximizes $J(w)$
	- $$J(w) = \frac{w^{T}S_{B}w}{w^{T}S_{W}w} = \frac{|w^{T}(m_{1} - m_{2})|^2}{w^{T}S_{W}w}$$
- Taking partial derivative with respect to $w$
	- $$w = c.S^{-1}_{w}(m_{1} - m_{2})$$
- As $w$ is the required direction and not magnitude, consider and find $w$
- Parametric Solution
	- $$w = \sum^{-1}(\mu_{1} - \mu_{2})$$
	- when $p(x|C_{i}) \sim N\left( \mu_{i}, \sum \right)$

