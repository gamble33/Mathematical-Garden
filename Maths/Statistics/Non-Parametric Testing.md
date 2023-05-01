```ad-definition
A **parameter** is a definition, i.e., something that controls the population

> [!example]
> Mean, variance, probability, skew
```

```ad-definition
A **Non-Parameter** is an observation of the population.

> [!example]
> median, mode, IQR
```

![[Pasted image 20230313160256.png]]

# Single Sample Sign test
Given a random sample of a population, $50\%$ of the data would be expected to be above the median.

Therefore, this leads to a probability of $0.5$ for any given data-point being above this median.

Introducing the statistic $X$ which is the number of data-point counted above the suspected median.

$$X\sim B(n, 0.5)$$

where $n$ is the number of data-points in the sample.

We can measure the actual number of data-points found the be above the median and calculate the probability of this based on the distribution of $X$. This probability allows us to construct a hypothesis test for any given significance level.

```ad-example
The weights of 10 adults from a city are recorded in the table below:

| 57.0 | 59.7 | 75.4 | 92.9 | 108.8 |
| --- | --- | --- | --- | --- |
| 66.0 | 96.0 | 67.6 | 42.8 | 70.7 |

It is suspected that the adults of this city have a positive skew for their weight.

It is known that the mean weight is 85kg. Test at the 5% significance level whether there is in fact a positive skew.

Hypotheses:
---
$$H_0: \text{median} = 85$$
$$H_1: \text{median} \lt 85$$

Test Statistic:
---
Number of data below mean:
$$x=7$$
$$X\sim B(10, 0.5)$$
$$P(X \geq 7)=17
\%$$

Comparison:
---
$$17\% > 5\%$$

Insufficient evidence to reject the null hyptoiehtsis.
```

```ad-example
The Silicon Valley Bank, FL Branch manager indicates that the median number of savings account customers per day is $64$. A clerk from the same branch claims that it was more than $64$. The clerk collected the number of savings account customers per day data for $10$ random days. Can we reject the branch manager's claim at a $5\%$ significance level.

| Day       | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   | 10  |
| --------- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Customers | 60  | 66  | 65  | 70  | 68  | 72  | 46  | 76  | 77  | 75  |

Hypotheses:
---
$H_0:$ The median number of customers is $64$.
$H_1:$ The median number of customers is more than $64$.

Test Statistic:
---
Number of data above median, $x$, is:
$$x=8$$
$$X\sim B(10,0.5)$$
$$P(X \geq 8)=0.0547=5.47\%$$

Comparison:
---
$$5.47\% \gt 5\%$$

Conclusion:
---
Insufficient evidence to reject $H_0$. The median number could well be $64$.
```

# Wilcoxon signed-rank test
If we are given a single sample of continuous, indpendent data and we suspect it may fit a symmetric distribution, we can improve the rigour of our test.

Not only should we be counting how many data lie above or below our suspected median, we should also be considering 'how far' they deviate.

## How to Calculate the Test Statistic

Step 1) Compare each data point to the proposed median.

Step 2) Identify the rank of each difference where the smallest difference is rank $1$ and the greatest difference is rank $n$.

Step 3) Segregate the ranks into positives and negatives

Step 4) Calculate the sum of positive and negative ranks.

Step 5) The test statistic $t$ is the smaller of the two.

```ad-note
The sum of positive ranks and negative ranks must equal $$\frac{n(n+1)}{2}$$
```

```ad-example
The times ($ms$) taken by a computer to preform a certain task were recorded on $10$ randomly chosen occasions. The times were as follows.

| Times |
| ---   |
| $6.44$  |
| $6.16$  |
| $5.62$  |
| $5.82$  |
| $6.51$  |
| $6.62$  |
| $6.19$  |
| $6.42$  |
| $6.34$  |
| $6.28$  |

It has been claimed that the median time is $6.40\ ms$.

Carry out a Wilcoxon signed-rank test at the $5\%$ significance level to test this claim.

Hypotheses:
---
$H_0:$ The median is $6.40$
$H_1:$ The median is not equal to $6.40$

Test Statistic:
---
| Times  | Differences | $+$ Ranks | $-$ Ranks |
| ------ | ----------- | --------- | --------- |
| $6.44$ | $+0.04$     | 2         |           |
| $6.16$ | $-0.24$     |           | 8         |
| $5.62$ | $-0.78$     |           | 10        |
| $5.82$ | $-0.58$     |           | 9         |
| $6.51$ | $+0.11$     | 4         |           |
| $6.62$ | $+0.22$     | 7         |           |
| $6.19$ | $-0.21$     |           | 6         |
| $6.42$ | $+0.02$     | 1         |           |
| $6.34$ | $-0.06$     |           | 3         |
| $6.28$ | $-0.12$     |           | 5         |
| Total  |             | 14        | 41        |

$$t=14$$

Critical Value:
---
> [!note]
> This test is two-tailed.

$$T_{(10,0.05)}=8$$

Comparison:
---
$$14 \gt 8$$

Conclusion:
---
Insufficient evidence to reject $H_0$. The claim has not being disproved.

> [!note]
> This does not mean that the claim is true, it just means it has not been disproved.
```

```ad-observation
Assume all data points lie above a specified mean. The sum of ranks therefore, would simply be $\frac{n(n+1)}{2}$ and $0$. This represents a maximally biased spread. 

Given that we choose the lower value, the most biased value is represented by a $0$.
\
Alternatively, assume the data is fairly spread. I.e., both ranks are equal and both take a value of $\frac{n(n+1)}{4}$. We can see that a maximally fair system has a higher value of $t$.

This is why our cirtical value is a lower bound of "acceptable" rank sums. That is, if our rank sum is less than the critical value, then the null hypothesis can be rejected.
```

```ad-example
Metal rods produced by a certain factory are claimed to have am edian breaking strength of $200$ tonnes. For a random sample of $9$ rods, the breaking strenghts, measured in tonnes, were as follows.

$$\begin{matrix} 210 && 186 && 188 && 208 && 184 && 191 && 215 && 198 && 196 \end{matrix}$$

A scientist believe that hte median breaking strength of metal rods produced by this factory iss less than $200$ tonnes.

(a) Use a Wilcoxon signed-rank test, at the $5\%$ significance level, to test whether there is evidence to support the scientist's belief.

Hypotheses:
---
$H_0:$ The median breaking strength is equal to $200$ tonnes.
$H_1:$ The median breaking strength is lower than $200$ tonnes.

Test Statistic:
---
| Times | Differences | Ranks | $+$Ranks | $-$Ranks |
| ----- | ----------- | ----- | -------- | -------- |
| $210$ | $+10$       | 5     | 5        |          |
| $186$ | $-14$       | 7     |          | 7        |
| $188$ | $-12$       | 6     |          | 6        |
| $208$ | $+8$        | 3     | 3        |          |
| $184$ | $-16$       | 9     |          | 9        |
| $191$ | $-9$        | 4     |          | 4        |
| $215$ | $+15$       | 8     | 8        |          |
| $198$ | $-2$        | 1     |          | 1        |
| $196$ | $-4$        | 2     |          | 2        |
| Total |             |       | 16       | 29       |

$t=16$

Critical Value:
---

> [!note]
> This test is one-tailed.

$$T_{(0.05, 9)}=8$$

Comparison:
---
$$16 \gt 8$

Conclusion:
---
Insufficient evidence to reject $H_0$.

(b) Why is a Wilcoxon signed-rank test preferable to a sign test even though both are valid.


```

# Paired sample sign test
If we're given a sample frame where two measurements are taken then we are able to apply a paired sample sign test.

```ad-definition
A **sample** is a collection of data from the population.

A **sample frame** is a collection of sampling units from the population.

Each **smapling unit** is one article that can create a data point. 

Sampling units can create multiple data points for **paired samples**.
```

Between these two paired sample, we often look for a systematic difference between the two. Generally, our starting point is to assume no statistic difference ;) ;) This will be our null hypothesis.

If we assume there is no systematic difference then there should be a $50\%$ chance of either the first or second sample being higher. Therefore, we are able to use a binomial test.

```ad-example
The time taken for $9$ children to tie their sholaces is recorded in seconds. Use a paired sample sign test to measure if there is a significant difference between the time taken to tie the left and right laces. Test at the $10\%$ signifiance level.

| Child     | Left Shoe | Right Shoe | Left Slower |
| --------- | --------- | ---------- | ----------- |
| Alfie     | 42        | 45         | +           |
| Betty     | 38        | 36         | -           |
| Carl      | 51        | 52         | +           |
| Debby     | 42        | 39         | -           |
| Ed        | 31        | 35         | +           |
| Francesca | 48        | 49         | +           |
| George    | 61        | 62         | +           |
| Harriet   | 38        | 39         | +           |
| Isaac     | 44        | 45         | +           |

Hypotheses:
---
$H_0:$ There is no difference.
$H_1:$ There is a difference.

Test Statistic:
---
Count the number of times the Left Shoe was slower
$$x=2$$
$$X\sim B(9, 0.5)$$
The expected number of times that the left shoe would be slower is $4.5$.
$$P(X \leq 2)=0.0898$$

Comparison:
---
The test is two-tailed thus our significance level is halved.
$$8.98\% \gt 5\%$$

Conclusion:
---

We have insufficient evidence to reject $H_0$.
```



# Wilcoxon matched-pairs signed-rank test
Sometimes, there is no reason to assume that a sample forms a symmetric distribution. In this case, the distribution of the differences of paired sampels (which are assumed to have an expected value of $0$) can be assumed to be symmetric.

Thus, we can perform a Wilcoxon signed-rank test on the differnces of the matched pairs.

```ad-note
We can also assume the distribution of differences is symmetric if the underlying distributions are identical but for a translation.

These distributions can be asymmetric as long as they have an identical shape.
```

```ad-example
We have the following data on the probability of ear infections on swimmers before and after taking a medication that is hypothesized to prevent infections. Test, at the $5\%$ significance level, if the reduction in infections is significant.

| Swimmer | Probability before | Probability after | Differences | Ranks | $+$Ranks | $-$Ranks |
| ------- | ------------------ | ----------------- | ----------- | ----- | -------- | -------- |
| A       | 0.3                | 0.24              | -0.06       | 3     |          | 3        |
| B       | 0.01               | 0.16              | +0.15       | 6     | 6        |          |
| C       | 0.52               | 0.47              | -0.05       | 2     |          | 2        |
| D       | 0.44               | 0.05              | -0.39       | 10    |          | 10       |
| E       | 0.29               | 0.18              | -0.11       | 5     |          | 5        |
| F       | 0.47               | 0.37              | -0.10       | 4     |          | 4        |
| G       | 0.35               | 0.16              | -0.19       | 8     |          | 8        |
| H       | 0.55               | 0.32              | -0.23       | 9     |          | 9        |
| I       | 0.21               | 0.2               | -0.01       | 1     |          | 1        |
| J       | 0.16               | 0.34              | +0.18       | 7     | 7        |          |
| Totals  |                    |                   |             |       | 13       | 42       | 

Hypotheses:
---
$H_0$: There is no reduction in infections.
$H_1$: There is a reduction in infections.

Test Statistic:
---
$$x=13$$

Critical Value:
---
$$T_{(0.95, 10)}=10$$

Comparison:
---
$$13 \gt 10$$

Conclusion:
---
Insufficient evidence to reject $H_0$. There is no reduction in infections.


```



# Wilcoxon rank-sum test
This is used for a two-sample system where the samples are not paired. This is still valid even if the samples are not of the same size.

The key assumption is that all of the data comes from the same population distribution. The type of distribution is unknown, therefore, a parametric test cannot be performed. However, we can perform a non-parametric test, looking at a sub-group.

## Test Statistic
$$W$$
To find the test statistic, $W$, we use $m$ and $n$.

$m$ and $n$ are the  sample sizes of subsets $M$ and $N$ respectively. $m$ being the smaller one.

We calculate the rank sum from the subset $M$.

$$W=\min(R_M, m(n+m+1)-R_M)$$

The statistic $W$ is the minimum of the sum of ranks when measured small to large or large to small. By doing it this way, we are able to isolate the rank sum of the smaller subsets regardless of whether it is larger or smaller than the population as a whole.

This test statistic should be compared with a critical value from the lookup table. Crucially, we need to be lower than a critical value in order to reject the null hypothesis.

```ad-example
During the 2012 Olympics, th times for the Men's 100m Semi-finals were recorded, and the athletes who compelted the race in under 10.1 seconds are given bwlow. Use a $5\%$ significance level to determine if athletes from the Caribbean are generally faster than those from outside.

In the case of our data, the sub-group is the males that come from the Caribbean.

Hypotheses:
---
$H_0:$ Elite athletic men run 100m in a time which is independent of origin (race/nationality).
$H_1:$ Being from the Caribbean makes you faster (decreases your time).

Test Statistic:
---

| Caribbean? | Time  | Caribbean Ranks | Non-Caribbean Ranks |
| ---------- | ----- | --------------- | ------------------- |
| No         | 9.82  |                 | 1                   |
| Yes        | 9.85  | 2               |                     |
| Yes        | 9.87  | 3               |                     |
| No         | 9.9   |                 | 4                   |
| No         | 9.91  |                 | 5                   |
| Yes        | 9.94  | 6               |                     |
| No         | 9.96  |                 | 7                   |
| Yes        | 10.02 | 8               |                     |
| Yes        | 10.04 | 9               |                     |
| No         | 10.05 |                 | 10                  |
| No         | 10.06 |                 | 11                  |
| Yes        | 10.08 | 12              |                     |
| No         | 10.09 |                 | 13                  |
| Total      |       | 40              | 51                  |

$$m=6$$
$$n=7$$
$$R_M=40$$

$$W=\min(40,44)=40$$

Critical Value:
---
$$W_{\text{crit}}=29$$

Comparison:
---
$$40\gt29$$

Conclusion:
---
Insufficient evidence to reject $H_0$. Eugenics have been disproved.
```

```ad-summary
1. Hypothesize a difference.
2. Find $R_M$ (rank sum of the sample with a lower sample size)
3. Find $m(n+m+1) - R_M$.
4. Think: is $\left[R_M\right]$ or $\left[m(n+m+1) - R_M\right]$ smaller? The statistic $W$ takes the value of the smaller value.
5. Look up $W_{\text{crit}}$.
6. Compare.
```

## If $n$ and/or $m$ are too large.
For larger values of $m$ and $n$, a normal approximation can be used.

$$R_M\sim N\left(\frac12m(m+n+1),\frac1{12}mn(m+n+1)\right)$$

Use the normal hypothesis test protocol.