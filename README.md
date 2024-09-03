<h1>Multiple Linear Regression</h1>

<h2>Introduction</h2>

*Multiple linear regression is a linear regression with more than one predictor.* 

In general we write the model as follows:

$$y = \beta_0 + \beta_1 x_1 + \beta_2 x_2  + \ldots + \beta_n x_n $$

where, similarly to the simple linear regression:

  - $y$ is the **response**, or the dependent variable
  - $x_1, x_2,\ldots, x_n$ are the **predictors**, aften called the independent or explanatory variables 
  - $\beta_0$ is the **intercept** and $\beta_1, \beta_2, \ldots, \beta_n$ are the **regression coefficients**
  - $n$ is the number of predictors used, often referred to as a model's **degrees of freedom**

In addition to the assumptions discussed with respect to the simple linear regression, application of multiple linear regression assumes that *the individual **predictors are independent** of each other*.


<h2>How to evaluate multiple linear regression model?</h2>

Similarly to simple linear regression, we must inspect the model residuals first. Residuals must be approximately normally distributed with mean close to zero. To assess the independence of the model residual, we may plot the dependence of the residuals on the values of each of the model predictors.

To evaluate the multiple linear regression model, we can apply the measures that were previously described, such as $R^2$, RMSE, etc.. 
However, a regression *model with more predictors will always have a better $R^2$ and RMSE*. 

This is because increased number of predictors increases number of parameters that can be tuned, so that the obtained $\hat{y}$ estimates are closer to true $y$ values. 

To account for this fact, we may need to use **adjusted $R^2$**,

$$R_\text{adj}^2 = 1 - (1 - R^2)\frac{n - 1}{n - k - 1}$$

where:

  - $R^2$ is the unadjusted coefficient of determination
  - $n$ is the number of observations
  - $k$ is the number of model's degrees of freedom

Importantly, unlike adjusted $R^2$, there is no adjusted form of RMSE that would account for the number of predictors.
