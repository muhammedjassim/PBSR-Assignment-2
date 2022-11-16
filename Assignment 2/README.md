# Probability and Statistics with R - Assignment 2

## Group Members
* Muhammed Jassim (MDS202220)
* Anusha R (MDS202212)
* Narendran Ramakrishnan (MDS202221)

### Problem 1

We derive a pdf from the given geometric sequence by defining the required changes. The derived pdf turns out to be that of Geometric distribution. Hence the mean and variance must exist. We analytically derived the mathematical expression for mean and variance. From the given summary statistics we found the parameters for the distribution and compared it with Poisson distribution. Poisson seemed to be the better fit as the variance is lower and central tendency values are also in the vicinity of the expected values.

### Problem 2

We defined a function which returns the MLE of $\log{\alpha}$, where $\alpha$ is a parameter of $\Gamma(\alpha,\sigma)$. We utilized the inbuilt `optim` function in `R` for this. We sampled 20 random points from $\Gamma(\alpha,\sigma)$ for given values of the parameters and found the MLE of $\log{\alpha}$ using the defined function. We did this 1000 times and plotted the histogram of MLE's obtained. The MLE value with maximum frequency was observed to be approximately $\log{\alpha_0}$ where $\alpha_0$ is the value of parameter $\alpha$ using which we generated the datapoints. We repeated the process with different sample sizes and observed that as the sample size increase, the gap between $2.5^{th}$ and $97.5^{th}$ decreased, implying the distribution getting more accurate to the true value.

### Problem 3

We were tasked with fitting the `faithful` dataset using 3 mixed probability models which were combinations of Gamma & Normal, Gamma & Gamma, and LogNormal & LogNormal respectively. In each case we fit the models using MLE method and calculated the corresponding _Akaike Information Criterion (AIC)_.The density plot corresponding to each model was also plotted above the histogram of the real data to demonstrate the goodness of fit. We reported the model with least AIC value as the model of best fit and using the same model we calculated the probability $\mathbb{P}(60 < X <70)$.

### Problem 4

We were tasked to fit different linear regression models on data given to us using different distributional assumptions on the errors. We considered 4 distriubtions: Normal, Laplace, Lognormal and Gamma, and for each of the 4 cases, we used `optim` in `R` to find the MLE of the parameters. We also calculated the BIC for the models and based on it, found that the model with $\epsilon_i \sim \text{Laplace}(0,\sigma^2)$ gave the lowest BIC. The regression lines were plotted over the scatter plot of the data to visually depict the goodness of fit.

### Problem 5

We were tasked with estimating the parameters of linear regression between log return of TCS and NIFTY. We carried out the estimation using Method of moments plug-in estimators and also using the `lm` function of `R`. The plug-in estimators are:
* $\beta = \frac{Cov(X, Y)}{Var(X)}$
* $\alpha = \hat{Y} - \beta \hat{X}$
* $\sigma = \sqrt{Var(Y) - \beta^2 Var(X)}$

We also utilised the regression line to predict the value of TCS log returns based on NIFTY log returns.
