- $$Accuracy = \frac{TP}{(TP+TN)}$$
- $$\mathrm{Recall} = \frac{TP}{TP+FN}$$
- $$\mathrm{Precision} = \frac{TP}{TP+FP}$$
- $$F-1 \  Score = \frac{1}{f} = \Bigg(\frac{1}{R} + \frac{1}{P}\Bigg)$$
- $$R^{2}= 1- \frac{^{SS}Regression}{^{SS}Total} = 1 - \frac{\sum_{i} (y_{i} - \bar{y_{i}})^2}{{\sum_{i}(y_{i} - \bar{y})^2}}$$
- $$Mean \ Square \ Error = MSE = \frac{1}{n}\sum_{t=1}^{n}e^2_{t}$$
- $$Root \ Mean \ Square \ Error = RMSE = \sqrt{ \frac{1}{n}\sum_{t=1}^{n}e^2_{t}}$$
- $$Mean \ Absolute \ Error = MAE = \frac{1}{n}\sum_{t=1}^{n}|e_{t}|$$
- $$Mean \ Absolute \ Precentage \ Error = MAPE = \frac{100\%}{n}\sum_{t=1}^{n}\Bigg|\frac{e_{t}}{y_{t}}\Bigg|$$
- $$w_{0} = \bar{y} - w_{1}\bar{x}$$
- $$w_{1} = \frac{{\sum \frac{y_{i}x_{i}}{N}}-\bar{y}\bar{x}}{\sum \frac{x_{i}^{2}}{N}-\bar{x}^2}$$
- $$\bar{x} = \frac{\sum_{i}^nx_{i}}{N}$$
- $$PDF = p(x|C_{i}) = \frac{1}{\sqrt{ s\pi }\sigma_{i}}\exp\Bigg[-\frac{(x-{\mu^{2}_{i})}}{2\sigma_{i}^{2}}\Bigg]$$
- $$Log \ Likelihood = L(\mu, \sigma|X) = -\frac{N}{2}\log(2\pi) - N\log \sigma - \frac{\sum_{t}(x^t-\mu)^2}{2\sigma^2}$$
- $$Baye's \ Theorem = P(C_{i}|x) = \frac{{p(x|C_{i})P(C_{i})}}{\sum_{k=1}^{K}p(x|C_{k})P(C_{k})}$$

---
To estimate the **probability density function (PDF)** at x=170x = 170x=170 cm using a nonparametric method, such as the **kernel density estimator (KDE)**, we can proceed step-by-step. Since you mentioned using the **cumulative distribution function (CDF)**, we'll use that for calculating the PDF by applying the concept:

$$f(x)=dF(x)dxf(x) = \frac{dF(x)}{dx}f(x)=dxdF(x)​$$

### Step-by-Step Solution:

1. **Data Points:** The dataset consists of heights of 10 people:  
    X={150,155,160,165,170,175,180,185,190,195}X = \{150, 155, 160, 165, 170, 175, 180, 185, 190, 195\}X={150,155,160,165,170,175,180,185,190,195}.
    
2. **CDF Approximation:** The CDF at a point xxx is the proportion of data points less than or equal to xxx. You can estimate the CDF empirically for each data point by calculating the cumulative probability for each height.
    
    The CDF at any given height xix_ixi​ in an ordered dataset XXX can be defined as:
    
    $$F(xi)=inF(x_i) = \frac{i}{n}F(xi​)=ni​$$
    
    where iii is the index of the data point in the sorted dataset, and nnn is the total number of data points.
    
    For x=170x = 170x=170 cm, we calculate the CDF as follows:
    
    - There are 5 data points less than or equal to 170 (150, 155, 160, 165, 170).
    - The empirical CDF at 170 is:
    
    F(170)=510=0.5F(170) = \frac{5}{10} = 0.5F(170)=105​=0.5
3. **Estimate PDF:** The PDF at xxx can be approximated by taking the derivative of the CDF. However, since we have discrete data, we can estimate the PDF by calculating the difference between adjacent CDF values:
    
    f$$(x)≈F(x+h)−F(x−h)2hf(x) \approx \frac{F(x+h) - F(x-h)}{2h}f(x)≈2hF(x+h)−F(x−h)​$$
    
    where hhh is a small bandwidth around the point of interest. Using adjacent data points x=165x=165x=165 and x=175x=175x=175 around 170:
    
    - $$F(165)=410=0.4F(165) = \frac{4}{10} = 0.4F(165)=104​=0.4$$
    - $$F(175)=610=0.6F(175) = \frac{6}{10} = 0.6F(175)=106​=0.6$$
    
    The approximate PDF at x=170x = 170x=170 cm is:
    
    $$f(170)≈0.6−0.42(5)=0.210=0.02f(170) \approx \frac{0.6 - 0.4}{2(5)} = \frac{0.2}{10} = 0.02f(170)≈2(5)0.6−0.4​=100.2​=0.02$$
    
    Therefore, the estimated PDF at x=170x = 170x=170 cm is $0.02\text{cm}^{-1}.$
    
---
