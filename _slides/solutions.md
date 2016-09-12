---
---

## Exercise solutions

<!--split-->

### Solution 1


~~~r
species <- c()
count <- c()
data <- data.frame(species, count)
~~~
{:.text-document title="lesson-2.R"}


~~~r
str(data)
~~~
{:.input}
~~~
'data.frame':	0 obs. of  0 variables
~~~
{:.output}

<aside class="notes" markdown="block">

[Return](#exercise-1)

</aside>

<!--split-->

### Solution 2


~~~r
sol2a <- days[c(-1, -7)]
sol2b <- days[seq(2, 7, 2)]
~~~
{:.text-document title="lesson-2.R"}


~~~r
sol2a
~~~
{:.input}
~~~
[1] "Monday"    "Tuesday"   "Wednesday" "Thursday"  "Friday"   
~~~
{:.output}


~~~r
sol2b
~~~
{:.input}
~~~
[1] "Monday"    "Wednesday" "Friday"   
~~~
{:.output}

<aside class="notes" markdown="block">

[Return](#exercise-2)

</aside>

<!--split-->

### Solution 3


~~~r
sol3 <- df[2:3, 'ed']
~~~
{:.text-document title="lesson-2.R"}


~~~r
sol3
~~~
{:.input}
~~~
[1] highschool college   
Levels: middle < highschool < college
~~~
{:.output}

<aside class="notes" markdown="block">

[Return](#exercise-3)

</aside>

<!--split-->

### Solution 4


~~~r
df <- data.frame(
    size = 1:5,
    year = factor(
        c(2014, 2014, 2013, 2015, 2015),
	levels = c(2013, 2014, 2015),
	ordered = TRUE),
    prop = runif(n = 5))
fit <- lm(prop ~ size + year, data = df)
~~~
{:.text-document title="lesson-2.R"}


~~~r
summary(fit)
~~~
{:.input}
~~~

Call:
lm(formula = prop ~ size + year, data = df)

Residuals:
         1          2          3          4          5 
 2.211e-01 -2.211e-01 -1.388e-17 -2.211e-01  2.211e-01 

Coefficients:
             Estimate Std. Error t value Pr(>|t|)
(Intercept)  0.668251   1.343065   0.498    0.706
size        -0.052918   0.442262  -0.120    0.924
year.L      -0.264598   0.605592  -0.437    0.738
year.Q       0.009804   0.879904   0.011    0.993

Residual standard error: 0.4423 on 1 degrees of freedom
Multiple R-squared:  0.4792,	Adjusted R-squared:  -1.083 
F-statistic: 0.3067 on 3 and 1 DF,  p-value: 0.8313
~~~
{:.output}

<aside class="notes" markdown="block">

[Return](#exercise-4)

</aside>
