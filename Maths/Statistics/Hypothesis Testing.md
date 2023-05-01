#Todo #Statistics #Maths 

# Hypothesis Testing
---
## Hypothesis
A Hypothesis is a statement made about the value of a **population parameter** that we wish to test by collecting evidence in the form of a sample.
* The null hypothesis, $H_0$, is the default position, i.e., that nothing has changed, unless proven otherwise.
* The alternative hypothesis, $H_1$, is that there has been some change in the population parameter.

## Test statistic
In a hypothesis test, the evidence from the sample is a test statistic.

## Level of significance
The level of significance, $\alpha$, is the maximum probability where we would reject the null hypothesis. This is usually $5\%$ or $1\%$.

## Critical Region
The range of values of the test statistic that would lead to you rejecting $H_0$.

## Critical Values
The values on the boundary of the critical region are called critical values.

## Actual Significance Level
The actual probability of being in the critical region.

## Example Question
John tosses a coin 8 times and it comes up heads 6 times. He claims the coin is biased towards heads. With a significance level of 5%.

### STEP 1
Define test statistic $X$ (stating its distribution and the parameter $p$.)

$X$ is the number of heads.
$p$ is the probability of heads.
$X~B(8, p)$
### STEP 2
Write null and alternative hypothesis

$H_0:p=0.5$
$H_1:p>0.5$

### STEP 3
Determine probability of observed test statistic (or 'more extreme'), assuming null hypothesis. I.e., determine probability we'd see this outcome just by chance.

Assume $H_0$ is true, $X~ B(8, 0.5)$.
$$P(X\geq 6) = 1 - P(X \geq 5)$$
$$=1-0.8555$$
$$=0.1445$$
Alternatively,
$$P(X \geq 7) = 1 - 0.0352$$
Critical region is $X \geq 7$.
6 is not in critical region, so do not reject $H_0$.
### STEP 4
Two-part conclusion
1. Do we reject $H_0$ or not?
2. Put in context of original problem.

$14,45\% > 5\%$, so, insufficient evidence to reject $H_0$.
We can assume the coin is not biased.

## Actual Level of Significance
The probability of rejecting $H_0$ under stated parameters.

## Hypothesis Testing on the Sample Mean
$$\bar{X} \sim N(\mu, \frac{\sigma^2}{n})$$
## Errors
### Type I Error
To **incorrectly** reject $H_0$ is known as a **Type I Error**. The probability of a Type I error is the actual significance level of the hypothesis test.
### Type II Error
To **incorrectly** <u>accept</u> $H_0$ is known as a **Type II Error**

### Summary
![[Pasted image 20220527151742.png|500]] #Todo
## Summary
1. Identify population parameter $\theta$ (use proportion $p$ in Binomial or mean rate $\lambda$ for a Poisson) you are going to test.
2. Write $H_0$ and $H_1$. Consider whether test is one or two tailed.
3. Specify significance level $\alpha$ (usually 0.05 or 0.01).
4. Find out whether observed value $x$ of your test statistic falls in critical region.
	1. One tail:
		1. $H_0:\theta = m$, $H_1:\theta > m$ --> Reject $H_0$ if $P(X \geq x) \leq \alpha)$ or...
		2. $H_0:\theta = m$, $H_1:\theta < m$ --> Reject $H_0$ if $P(X \leq x) \leq \alpha)$
	1. Two tail:
		1. $H_0:\theta = m$, $H_1:\theta \neq m$ --> Reject $P(X \geq x) \leq \frac{1}{2}\alpha$ or $P(X \leq x) \leq \frac{1}{2}\alpha)$
5.  State conclusion. Address:
	1. Is result **significant or not**?
	2. What are the implications in terms of context of original problem

# Selecting a Hypothesis Test
```mermaid
graph LR
	i0("Do we know a model for the population distribution?") -->|"yes"| i1("do we know the\nparameters of the model?")
	i1 -->|"yes"| s0("derive test statistic from\nthe sample. (this is generally\n a sample mean or a\nfrequency of success).")
 subgraph sample testing
 s0 --> s1("compare this test statistic\nto the critical value.")
 end
 

	i0 -->|"maybe"| c0("are we testing\nindependence of\nbi-variate data?")
	subgraph Chai-Squared Testing
	 c0 -->|"no"| c3("are the parameters\nof the model being tested known?")
	 c3 -->|"no"| c5("estimate parameters using\nthe data.")
	 c5 --> c4
	 c3 -->|"yes"| c4("calculate the expected\nfrequencies based on the\nmodel.")
	 c4 --> c6("are any expected frequencies\nless than 5?")
	 c6 -->|"yes"| c7("group frequencies\ntogether.")
	  c6 -->|"no"| c8("calculate degrees of freedom, v.\nv=cells-constraints.\nconstraints can be:\n- estimated parameters\n- total number of values")
	  c7 --> c8
   c8 --> c2
   c2 --> c9("compare to critical value\n(found on the lookup table)\nand make conclusion.")
	c0 -->|"yes"| c1("calculate estimated frequencies\n based on the relative frequencies \nof the subgroups\nthe degrees of freedom, v, equals\n(r-1)(c-1)")
	c1 --> c2("calculate a goodness of fit measurement:\n(X^2=\sum \frac{O_i^2}{E_i} - N)")
	end

	i1 -->|"no"| i2("do we know the\nvariance of the sample?\n\n(we will generally\nbe testing for the\nmean.)")
	subgraph inferential statistics
	i2 -->|"yes"| i11("how many samples?")
	
	i11 -->|"1 sample"| i3("use sample mean\nand assumed population\nmean to calculte z-score.\n$z=\frac{\overline{x}-\mu_0}{\frac{\sigma}{\sqrt{n}}}$")
	 i11 -->|"2 paired samlpes"| i12("measure the difference\nbetween pairs.")
	 i12 --> i3
	  i11 -->|"2 unpaired samples"| i13("$z=\frac{\overline{x}-\overline{y}-\mu_d}{\sqrt{\frac{\sigma_x^2}{n_x}+\frac{\sigma_y^2}{n_y}}}$")
	  i13 --> i8
	 
	 i2 -->|"no"| i4("how large is the sample?")
	 i4 -->|"<25"| i5("sample variance\nis biased estimator\nfor population varaince.")
	 i5 --> i20("how many samples?")
	 
	 i20 -->|"1 sample"| i9("use sample mean\nand assumed population\nmean to calculte t-score.\n$t=\frac{\overline{x}-\mu_0}{\frac{S_n}{\sqrt{n}}}$")
	 i20 -->|"2 paired sample"| i21("find the mean of the differences & sample variance of differences")
	 i20 -->|"2 unpaired samples"| i23("added condition is\nthat we must assume\nthe samples come from\nthe same population.\ntherefore, we use\na combined sample\nvariance as an\nestimator.\n$t=\frac{(\overline{x}-\overline{y})-\mu_d}{S_c\sqrt{\frac{1}{n_x}+\frac{1}{n_y}}}$")
	  i23 --> i10
	 i21 --> i9
	 i9 --> i10("use t-test\nas lookup table.")
	 i4 -->|">=25"| i15("how many samples?")
	 i15 -->|"2 unpaired samples"| i16("$z=\frac{\overline{x}-\overline{y}-\mu_d}{\sqrt{\frac{S_x^2}{n_x}+\frac{S_y^2}{n_y}}}$")
	 i16 --> i8
	 i15 -->|"2 paired samples"| i17("measure differences")
	 i17 --> i6
	 i15 -->|"single sample"| i6("sample variance\nis an appropriate estimator\nfor population variance.")
	 i6 --> i7("use sample mean\nand assumed population\nmean to calculte z-score.\n$z=\frac{\overline{x}-\mu_0}{\frac{S_n}{\sqrt{n}}}$")
	 i7 --> i8("use normal distribution\nas lookup table.\nusinzg calculted z-score.")
	 i3 --> i8
	end
 
	
	i0 -->|"no"| id3("if we don't know the population distribution, \n we cannot test for any parametric value. \n However, we can test for non parametric values.")
	subgraph non-parametric tests
	id3 --> id4("are the sample(s) thought to be symmetric?")
 
	id4 -->|"yes (this is preferable\nbecause it takes magnitude of \ndifferences into account)"| id10("how many samples are there?")
	id10 -->|"single sample"| id11("assume a centile,\ne.g., the median.")
	id10 -->|"two paired samples"| id12("measure difference between them.")
	id10 -->|"two unpaired samples"| id13("perform wilcoxon signed rank test\n- use lookup table")
	id11 --> id14("perform a wilcoxon signed rank test\n- use lookup table")
	id12 --> id14
 
	id4 -->|"no"| id6("are there 2 paried samples?")
	id6 -->|"no"| id5("the hypothesis is an assumed centile.\ne.g., median")
	id6 -->|"yes"| id8("measure the difference between\nthem and assume the difference is zero.")
	id5 --> id9("perform a sign test\nusin a binomial distribution\nfor the test statistic.")
	 id8 --> id9
	 end
```