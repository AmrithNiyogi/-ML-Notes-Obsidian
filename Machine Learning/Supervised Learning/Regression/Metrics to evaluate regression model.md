- **R squared/Adjusted R square**:
	- how much of variability in dependent variable can be explained by the model. It is square of Correlation Coefficient (R) and that is why it is called R Square.
	- 
	- R Square value is between 0 to 1 and bigger value indicates a better fit between prediction and actual value.
- **Mean squared error** (MSE)
- **root mean squared error** (RMSE)
- **mean absolute error** (MAE)
- **mean absolute percentage error** (MAPE)



$$MSE = \frac{1}{n} \sum_{t=1}^{N} e^2_{t}$$
$$RMSE = \sqrt{ \frac{1}{n} \sum_{t=1}^{N} e^2_{t} }$$
$$MAE = \frac{1}{n} \sum^{N_{t=1}}|e_{t}|$$
$$MAPE = \frac{100\%}{n} \sum_{t=1}^{n}|\frac{e_{t}}{t}|$$

Example: 
Linear Regression

| Living area | # bedrooms | Price |
| ----------- | ---------- | ----- |
| 2104        | 3          | 400   |
| 1600        | 3          | 330   |
| 2400        | 3          | 369   |
| 1416        | 2          | 232   |
| 3000        | 1          | 540   |
| ...         | ...        | ...   |


- **Hypothesis**: y is a linear function of x
$$h_{\theta}(x) = \theta_{0} + \theta_{1}x_{1} + \theta_{2}x_{2}$$
	- the '$\theta_{i}$'s are the **parameters** (also called **weights**)