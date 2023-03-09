First statement of fact: Life does not give you a model. There is a true value, we will never know what it is. 

In order to start constructing a model, we collect data. From that data, we make estimations from the parameters of the model. E.g., sample mean gives an estimator of the true mean. However, the data does not tell us what model to use, only what parameters to use in the model. Therefore, we must make an informed guess about which model to use (a safe guess is often a normal distribution because most things are a normal distribution, but not always). Thus, it is useful to have a tool to test the appropriateness of the model.

# Understanding $\chi^2$ by example
Is a dice fair?

In order to test this, we are going to roll a dice $120$ times and observe the outcomes of those roles. We will then comapre these observed outcomes to what we expedcted to happen.

| Number                                        | $1$  | $2$  | $3$  | $4$  | $5$  | $6$  |
| --------------------------------------------- | ---- | ---- | ---- | ---- | ---- | ---- |
| Observed $$O_i$$                              | $23$ | $15$ | $25$ | $18$ | $21$ | $18$ |
| Expected Frequency if the die is fair $$E_i$$ | $20$ | $20$ | $20$ | $20$ | $20$ | $20$ |

We make the assumption about the model that it is uniformly distributed.

In order to test the appropriateness of this model, we require a statistic which measures the goodness of fit between the observed data and the expected data. We call this ${\bf X}^2$ 

> [!danger]
> The goodness of fit, ${\bf X}^2$ is a standalone symbol.
> 
> ${\bf X}^2$ not the same as $\chi^2$ and it is not the same as the statistical variable, $X$, squared
 
$${\bf X}^2=\sum^n_{i=1}\frac{(O_i-E_i)^2}{E_i}$$

this can be simplifed:
$$\sum^n_{i=1}\frac{(O_i-E_i)^2}{E_i}=\sum^n_{i=1}\frac{O_i^2-2O_iE_i+E_i^2}{E_i}$$
$$=\sum^n_{i=1}\frac{O_i^2}{E_i}-2\sum^n_{i=1} O_i + \sum^n_{i=1} E_i$$
note that $\sum^n_{i=1} E_i$ and $\sum^n_{i=1} O_i$ will both be equal to the sample size. Let's call it $N$.

$$=\sum^n_{i=1}\frac{O_i^2}{E_i}-2N+N$$
$$=\sum^n_{i=1}\frac{O_i^2}{E_i}-N$$

notice that this statistic will not answer the question of "is this a uniform distribution?" Only how close is the sample to a uniform distribution.

As with any hypothesis test, we ask the question: "How close is close enough?"

Using the data provided, we calculate $${\bf X}^2=3.4$$

Consider the difference on any one outcome. How would we expect that to be distributed? As the expected frequency increases, the difference between the data and the expected value approaches a normal distribution as a result of the central limit theorem.

If we square the difference to ensures it is postive, then the distribitution will be the square of the normal distribution.

The sum of the squares of the normal distribution can be described with the standard result of the $\chi^2$ distribution. Notice that $\chi^2$ is not one single distribution but a collection of distributions which will depend on how many normal distributions are being summed.

In any situation, the degrees of freedom will be the variables that can change, i.e, there are no constraints. In our situation there are $6$ outcomes, however, the total number of data points is fixed. Therefore, knowledge about the first $5$ outcomes will constrain the $6^{\text{th}}$ outcome. Thus, there are $5$ degrees of freedom.

Considering our dice, we can test at the $5\%$ significance level whether or not the the observed frequencies could be modeleed as a discrete uniform distribution.

Hypothesis:
---
$H_0:$ The observed distribution can be modelled by a discrete uniform distribution (i.e., the die is not biased)

$H_1:$ The observed distribution cannot be modelled by a discrete uniform distribution (i.e., the die is biased)

Test Statistic:
---
$${\bf X}^2=3.4$$

Comparison:
---
$$\text{degrees of freedom}=5$$
$$\chi^2_{(0.95,5)}=11.07$$
$$3.4 \lt 3.4$$

Conclusion:
---
Thus, our test statistic is less than our critical value, therefore, we do not reject $H_0$. There is no evidence that the die is biased.

```ad-note
The degrees of freedom is the number of cells subtracted by the number of constraints.

In this case, the constraints refer to the datapoints where there is no choice (no freedom). 

E.g., if the number of data points is predetermined, then the first $n-1$ data points will determine (constrain) the $n^{\text{th}}$ data point.

E.g., if the expected value is predetermined, the $n-1$ data points will constrain the $n^{\text{th}}$ data point.
```

```ad-example
A 3-sided spinner is spun $150$ times, and counts of the three outcomes are shown. Test, aat the $1\%$ significance level, whether or not spinner is fair.

| Number   | 1   | 2   | 3   | Total |
| -------- | --- | --- | --- | ----- |
| Observed | 35  | 60  | 55  | 150   |

Hypothesis:
---
$H_0: \text{The observed distribution can be modelled by a discrete uniform distribution}$

$H_1: \text{The observed distribution cannot be modelled by a discrete uniform distribution}$

I.e., 
$H_0: \text{The spinner is fair}$

$H_1: \text{The spinner is biased}$

Test Statistic:
---
$${\bf X}^2=\frac{15^2}{50}+\frac{10^2}{50}+\frac{5^2}{50}=7$$

Comparison:
---
$$\chi^2_{(0.99,2)}=9.210$$
$$7 \lt 9.210$$

Conclusion:
---
$$7 \text{ is really big yo}$$
$$\text{but it aint as big as 9.210 ah ah ah}$$

$$\text{there4, }H_0\text{ cannot be rejected...}$$
```

```ad-danger
The goodness of fit test measurement tends not to work if the expected frequencies are less than 5.

This is because the goodness of fit relies on the central limit theorem in order to construct normal distributions that combine into a $\chi^2$ distribution.
```

# Testing a binomial distribution as a model
 
## Known Probabilities

```ad-example
THe data in the table is thought to be modeelled by a binomial $B \sim (10, 0.2)$. Use the table for the binomial cumulative distribution function to find expected values, and conduct a test to see if this is a good model. Use a $5\%$ significance level.

| $x$                | $0$  | $1$  | $2$  | $3$  | $4$ | $5$ | $6$ | $7$ | $8$ |
| ------------------ | ---- | ---- | ---- | ---- | --- | --- | --- | --- | --- |
| Observed Frequency | $12$ | $28$ | $28$ | $17$ | $7$ | $4$ | $2$ | $2$ | $0$ |

Hypothesis:
---
$H_0: \text{observed distribution can be modelled by a binomial distribution with } n = 10, p = 0.2$

$H_1: \text{observed distribution cannot be modelled by a binomial distribution with } n=10, p=0.2$

Test Statistic:
---
$N=\sum O_i=12+28+28+17+\dots=100$

> [!tip]
> Use Table feature on calculature and type in $f(x)=nCx\times p^x \times q^{n-x}$, $g(x)=x$

| $x$    | $0$      | $1$      | $2$      | $3$      | $4$      | $5$      | $6$      | $7$      | $8$      |
| ------ | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- |
| $P(x)$ | $0.1074$ | $0.2684$ | $0.3020$ | $0.2013$ | $0.0881$ | $0.0264$ | $0.0055$ | $0.0008$ | $0.0001$ | 

| $x$                | $0$     | $1$     | $2$    | $3$     | $4$    | $5$    | $6$    | $7$    | $8$    |
| ------------------ | ------- | ------- | ------ | ------- | ------ | ------ | ------ | ------ | ------ |
| Observed Frequency | $12$    | $28$    | $28$   | $17$    | $7$    | $4$    | $2$    | $2$    | $0$    |
| Expected Frequency | $10.75$ | $26.84$ | $30.2$ | $20.13$ | $8.81$ | $2.64$ | $0.55$ | $0.08$ | $0.01$ | 

> [!danger]
> SOME OF THE EXPECTED FREQUENCIES ARE LESS THAN $5$ AHHHHHH. 😮🥲😨😨😩🤯
>
> Thus, we group the tail end of the result to get an expected frequency greater than 5.

$$\downarrow$$

| $x$                | $0$     | $1$     | $2$    | $3$     | $\geq 4$ |
| ------------------ | ------- | ------- | ------ | ------- | -------- |
| Observed Frequency | $12$    | $28$    | $28$   | $17$    | $15$     |
| Expected Frequency | $10.75$ | $26.84$ | $30.2$ | $20.13$ | $12.09$  |

$${\bf X}^2=\frac{(12-10.75)^2}{10.75}+\frac{(28-26.84)^2}{26.84}+\dots=1.543$$

Comparison:
---
$$\chi_{(0.95,4)}^2=9.488$$
$$1.543 \lt 9.488$$

Conclusion: 
---
$$\therefore \text{insufficient evidence to reject null hypothesis} (H_0)$$
$$B(10,0.2) \text{ is a possible model for }O_i.$$

```

## Binomial Distribution for an unknown $p$
Consider a variable $X\sim B(n, p)$, and an experiment on $X$, repeated $N$ times.

If probability is unknown, we can estimate the probability from the data. To do this, we first consider the expected sample mean 
$$E(X)=p\times n$$
An unbiased estimator of $E(X)$ is given by $\overline{x}$
$$\overline{x}=p\times n$$
we can calculate $\overline x$ using the following formula
$$\overline{x}=\frac{\sum (xf)}{N}$$
thus,
$$\frac{\sum (xf)}{N}=p \times n$$
$$\implies p = \frac{\sum (xf)}{Nn}$$

```ad-warning
$n$ is the number of trials in an individual experiment.

$N$ is the number of experiments.
```

```ad-danger
Because, $p$ has now been calculated from the data, it adds a constraint. 

Therefore, this must be considered when calculating the degrees of freedom.
```

```ad-example
A study of the number of girls in families with five children was done on $100$ such families. The results are summarised in the following table.

| Number of girls ($r$) | $0$  | $1$  | $2$  | $3$  | $4$  | $5$ |
| --------------------- | ---- | ---- | ---- | ---- | ---- | --- |
| Frequency ($f$)       | $13$ | $18$ | $38$ | $20$ | $10$ | $1$ | 

Test at the $5\%$ significance level, whether or not a binomial distribution is a good model.

> [!thoughts]
> Why is binomial the best model to pick?
>
> Because we assume it satisfies the three criteria of a binomial distribution, which are:
>
> - Fixed number of trials,
> - Consistent and independent probabilities,
> - Binary outcome (success or failure) (boy or girl)

Hypothesis:
---
First, estimate the value of $p$.

$$p=\frac{(0\times13)+(1\times18)+(2\times38)+(3\times20)+(4\times10)+(5\times1)}{100\times5}$$

$H_0: \text{observed data can be modelled as a binomial distribution with }n=5, p=0.398$
$H_1: \text{observed data cannot be modelled as a binomial distribution with }n=5, p=0.398$

Test Statistic:
---
Find the expected frequencies (find the probabilities using the binomial distribution formula),

| Number of girls ($r$)                 | $0$     | $1$      | $2$      | $3$      | $4$      | $5$      |
| ------------------------------------- | ------- | -------- | -------- | -------- | -------- | -------- |
| Probabilities                         | $0.079$ | $0.2613$ | $0.3455$ | $0.2284$ | $0.0755$ | $0.0099$ |
| $\implies$ Expected Frequency ($E_i$) | $7.9$   | $26.13$  | $34.55$  | $22.84$  | $7.55$   | $0.99$   |

Group $4$ and $5$ as $5$'s expected frequency is less than $5$.

$$\downarrow$$

| Number of girls ($r$)      | $0$   | $1$     | $2$     | $3$     | $\geq 4$ |
| -------------------------- | ----- | ------- | ------- | ------- | -------- |
| Frequency ($f$)            | $13$  | $18$    | $38$    | $20$    | $11$     |
| Expected Frequency ($E_i$) | $7.9$ | $26.13$ | $34.55$ | $22.84$ | $8.54$   |

$${\bf X}^2=7.22$$

Comparison:
---
Find the degrees of freedom and lookup the critical value:
$$\text{degrees of freedom} = \text{cells (5) - N(1) - p(1)} = 3$$

$$\chi_{(0.95, 3)}^2=7.815$$
$$7.22 \gt 7.815$$


Conclusion:
---
$\text{insufficient evidence to reject }H_0.$

The observed data can be modelled as this binomial distribution with $n=5, p=0.398$.
```

```ad-example
![[Pasted image 20230309102729.png]]

a)
$$\frac{(0\times6)+(1\times16)+(2\times20)+(3\times23)+(4\times17)+(5\times10)+(6\times8)}{100}$$
$$=2.91$$

b)
$$p=\frac{\text{sample mean}}{\text{number of trials}}=\frac{2.91}{6}=0.485$$

$$P(X=3)=\left(\begin{matrix}6 \\ 3\end{matrix}\right)\times0.485^3\times(1-0.485)^{6-3}=0.312$$
$$\implies a = 0.3117 \times 100=31.17$$

$$P(x=6)=\left(\begin{matrix}6 \\ 6\end{matrix}\right)\times0.485^6\times(1-0.485)^{6-6}=0.013$$
$$\implies b = 1.30$$

c) 

Hypothesis:
---
$$H_0: \text{observed data can be modelled as a binomial distribution } B(6, 0.485).$$
$$H_1: \text{observed data cannot be modelled as a binomial distribution } B(6, 0.485).$$

Test Statistic:
---
Adjust classes such that no expected frequency is less than $5$.

| Number of defective items | $\leq 1$ | $2$   | $3$   | $4$   | $\geq 5$ |
| ------------------------- | -------- | ----- | ----- | ----- | -------- |
| Expected Frequency        | 12.41    | 24.82 | 31.17 | 22.01 | 9.59     |
| Observed Frequency        | 22       | 20    | 23    | 17    | 18       | 

$${\bf X}^2=\sum^n_{i=0}\frac{O_i^2}{E_i}-N=19.00$$

Comparison:
---
$$\chi_{(0.95, 3)}=7.815$$
$$19.00 \gt 7.815$$

Conclusion:
---
There is sufficient evidence to reject $H_0$. Thus, the data cannot be modelled as the binomial distribution, $B(6, 0.485)$.
```

# Testing a Poisson 🐠 distribution as a model
## Unknown value of $\lambda$.
```ad-definition
tu dis que tu vends mais tu la vends juste pour fume.

la suis dans l'espace, la suis dans l'espace.

j'me ballade sure paname.
```

The Poisson distribution measures the number of occurrences in a fixed space or time interval. It has a mean rate of $\lambda$ which leads to a variance of $\lambda$ and an expected value of $\lambda$. 

Thus, a good estimator of $\lambda$ is the sample mean.

```ad-example
The number of telephone calls arriving at an exchange in six-minute preiods were recorded over a period of $8$ hours, with the following results

| Number of calls ($r$) | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   |
| --------------------- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Frequency ($f$)       | 8   | 19  | 26  | 13  | 7   | 5   | 1   | 1   | 0   | 

Can these results be modelled by a Poisson distribution? Test at the $5\%$ significance level.
$$N=80$$
$$\lambda=\frac{176}{80}=2.2$$ 

Hypothesis:
---
$H_0:$ observed data can be modelled as a Poisson distribution with $\lambda=2.2$

$H_1:$ observed data cannot be modelled as a Poisson distribution with $\lambda=2.2$

Test Statistic:
---
| Number of calls ($r$) | 0            | 1            | 2            | 3            | 4            | 5             | 6            | 7              | 8              |
| --------------------- | ------------ | ------------ | ------------ | ------------ | ------------ | ------------- | ------------ | -------------- | -------------- |
| Probability $P(R=r)$  | 0.1108031584 | 0.2437669484 | 0.2681436432 | 0.1966386717 | 0.1081512694 | 0.04758655855 | 0.0174484048 | 0.005483784367 | 0.001508040701 |

| Number of calls ($r$)      | 0    | 1     | 2     | 3     | 4    | 5    | 6    | 7    | 8    |
| -------------------------- | ---- | ----- | ----- | ----- | ---- | ---- | ---- | ---- | ---- |
| Expected Frequency ($E_i$) | 8.86 | 19.50 | 21.54 | 15.73 | 8.65 | 3.81 | 1.40 | 0.44 | 0.12 |
| Frequency ($f$)            | 8    | 19    | 26    | 13    | 7    | 5    | 1    | 1    | 0    |

| Number of calls ($r$)      | 0    | 1     | 2     | 3     | 4    | $\geq 5$ |
| -------------------------- | ---- | ----- | ----- | ----- | ---- | --------------- |
| Expected Frequency ($E_i$) | 8.86 | 19.50 | 21.45 | 15.73 | 8.65 | 5.81            |
| Frequency ($f$)            | 8    | 19    | 26    | 13    | 7    | 7               |

$${\bf X}^2=2.09$$

Comparison:
---
$$\chi_{(0.95, 4)}=9.488$$
$$2.09 \lt 9.488$$

Conclusion:
---
There is insufficiente evidence to reject $H_0$, the distribution can be modelled by the Poisson distribution $\text{Po}(2,2)$.
```

# Contingency Tables

So far, we have been trying to decide which model best suits the data we have received. However, the data we have received comes from a single population. What if wanted to compare two variables of data to decide if the two variables are related?

|        |     | Grade |      |      | Totals |
| ------ | --- | ----- | ---- | ---- | ------ |
|        |     | $A$   | $B$  | $C$  |        |
| School | $X$ | $18$  | $12$ | $20$ | $50$   |
|        | $Y$ | $26$  | $12$ | $32$ | $70$   |
| Totals |     | $44$  | $24$ | $52$ | $120$  |

Determine to the $5\%$ significance level whether the school and grade are dependent.

If two variables are independent then the outcome of one has no effect on the outcome of the other. Another way to phrase this is to consider the probability of both variables. If $A$ and $B$ are independent variables then $P(A\cap B)= P(A)\times P(B)$. However, the probabilities cannot be known. Therefore, we use an estimator of the probability which is relative frequency.

Hypothesis:
---
$H_0:$  Grade and School are independent.

$H_1:$  Grade and School are not independent.

Test Statistic:
---
We still need to find a goodness of fit measurement between our observed data and expected model. In this case, the model is that our probabilities are independent. Therefore, we must find these probabilities; convert them into expected values, finally, calculate the difference between the observed values.

Probability table assuming independence:

|        |     | Grade                                |                                      |                                      | Totals            |
| ------ | --- | ------------------------------------ | ------------------------------------ | ------------------------------------ | ----------------- |
|        |     | $A$                                  | $B$                                  | $C$                                  |                   |
| School | $X$ | $\frac{50}{120}\times\frac{44}{120}$ | $\frac{50}{120}\times\frac{24}{120}$ | $\frac{50}{120}\times\frac{52}{120}$ | $\frac{50}{120}$  |
|        | $Y$ | $\frac{70}{120}\times\frac{44}{120}$ | $\frac{70}{120}\times\frac{24}{120}$ | $\frac{70}{120}\times\frac{52}{120}$ | $\frac{70}{120}$  |
| Totals |     | $\frac{44}{120}$                     | $\frac{24}{120}$                     | $\frac{52}{120}$                     | $\frac{120}{120}$ |

|        |     | Grade   |         |         | Totals |
| ------ | --- | ------- | ------- | ------- | ------ |
|        |     | $A$     | $B$     | $C$     |        |
| School | $X$ | $18.33$ | $10.00$ | $21.67$ | $50$   |
|        | $Y$ | $25.67$ | $14.00$ | $30.33$ | $70$   |
| Totals |     | $44$    | $24$    | $52$    | $120$  |

| $O_i$ | $E_i$ | $\frac{O_i^2}{E_i}$ |
| ----- | ----- | ------------------- |
| 18    | 18.33 | 17.676              |
| 12    | 10.00 | 14.4                |
| 20    | 21.67 | 18.46               |
| 26    | 25.67 | 26.334              |
| 12    | 14.00 | 10.286              |
| 32    | 30.33 | 33.76               |

$${\bf X}^2=0.916$$

Comparison:
---
```ad-important
$v=(h-1)(k-1)$

where:
- $v$ is the degrees of freedom
- $h$ is the number of rows of the table
- $k$ is the number of columns in the table
```

$$v=(2-1)(3-1)=2\times1=2$$
$$\chi_{(0.95,2)}^2=5.991$$
$$0.916 \lt 5.991$$

Conclusion:
---
Insufficient evidence to reject $H_0$. Therefore, there is insufficient evidence to say that the events are dependent.