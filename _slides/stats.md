---
---

## Distributions and Statistics

Since it is designed for statistics, R can easily draw random numbers from statistical distributions and calculate distribution values. 

To generate random numbers from a normal distribution, use the function `rnorm()`


~~~r
ten_random_values <- rnorm(n = 10)
~~~
{:.input}

| Function | Returns                                                      | Notes                     |
|----------+--------------------------------------------------------------+---------------------------|
| rnorm    | Draw random numbers from normal distribution                 | Specify `n`, `mean`, `sd` |
| pnorm    | Estimate probability of a specific number occuring           |                           |
| qnorm    | Cumulative probability that a given number or smaller occurs | left-tailed by default    |
| dnorm    | Returns quantile given a cumulative probability              | opposite of pnorm         |

Statistical distributions and their functions
See *Table 14.1* in **R for Everyone** by Jared Lander for a full table

| Distribution | Random Number |
|--------------+---------------|
| Normal       | rnorm         |
| Binomial     | rbinom        |
| Poisson      | rpois         |
| Gamma        | rgamma        |
| Exponential  | rexp          |
| Uniform      | runif         |
| Logistic     | rlogis        |

R has built in functions for handling many statistical tests. 


~~~r
x <- rnorm(n = 100, mean = 25, sd = 7)
y <- rbinom(n = 100, size = 50, prob = .85)
~~~
{:.text-document title="lesson-1.R"}


~~~r
t.test(x, y)
~~~
{:.input}

~~~
{:.input}

	Welch Two Sample t-test

data:  x and y
t = -23.819, df = 131.8, p-value < 2.2e-16
alternative hypothesis: true difference in means is not equal to 0
95 percent confidence interval:
 -18.93476 -16.03087
sample estimates:
mean of x mean of y 
 25.33719  42.82000 
~~~
{:.output}

Linear regression with the `lm()` function uses a formula notation to specify relationships between variables (e.g. `y ~ x`).


~~~r
fit <- lm(y ~ x)
~~~
{:.text-document title="lesson-1.R"}


~~~r
summary(fit)
~~~
{:.input}

~~~
{:.input}

Call:
lm(formula = y ~ x)

Residuals:
    Min      1Q  Median      3Q     Max 
-7.9295 -1.7776  0.2155  2.2345  5.9219 

Coefficients:
            Estimate Std. Error t value Pr(>|t|)    
(Intercept) 43.72354    1.08948  40.133   <2e-16 ***
x           -0.03566    0.04155  -0.858    0.393    
---
Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

Residual standard error: 2.805 on 98 degrees of freedom
Multiple R-squared:  0.00746,	Adjusted R-squared:  -0.002668 
F-statistic: 0.7366 on 1 and 98 DF,  p-value: 0.3928
~~~
{:.output}

<!--split-->

## Exercise

Create a data frame from scratch that has three columns and 5 rows. In column "size" place a sequence from 1 to 5. For column "year", create a factor with three levels representing the past three years. In column `prop`, place 5 random samples from a uniform distribution. Show the summary of a linear model following the formula "prop ~ size + year".