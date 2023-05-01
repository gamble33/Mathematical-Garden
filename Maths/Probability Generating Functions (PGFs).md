# Writing and Reading PGFs
```ad-definition
A **probability generating function** is an associated polynomial with positive coefficients that relate to a discrete probability distribution of integer values.

Using the probability generating funciton, we can make calculations and descriptions of the distributions. 
```

## Writing a PGF
First, consider a discrete random variable with probability mass function:
$$P(X=x_i)=k_i,\space\space\space\space x_i\in \mathbb{N}$$

$$G_X(t)=\sum k_i \times t^{x_i}$$
In other words, it is a power series (polynomial with increasing powers) where the coefficients are the probabilities of the associated outcomes which are the exponents.

$$P(x)=\left\{\begin{matrix}
0.3, & x=0\\
0.2, & x=1\\
0.5, & x=2
\end{matrix}\right\}=G_X(t)=0.3t^0 + 0.2t^1 + 0.5t^2$$

```ad-attention
What is $G_X(1)$?

$$G_X(1)=0.3+0.2+0.5=1$$

It is $1$. Matter of fact, $G$ of anything of $1$ must equal $1$. This is because the coefficients are the probabilities (which sum to $1$), therefore, when $1$ is the input, $1^n=1$, thus, $G_X(1)=1$.

What is $E(X)=0.3\times0+0.2\times1+0.5\times2=1.2$
$$E(X^2)=0.3\times0^2+0.2\times1^2+2^2\times0.5=2.2$$
$$E(t^X)=0.3t^0+0.2t^1+0.5t^2=G_X(t)$$
```

```ad-example
𝑋 is the discrete random variable that denotes the absolute difference of the scores where two fair dice are thrown. Construct the probability distribution of 𝑋 and write down the probability generating function.

$$P(x)=\left\{\begin{matrix}
\frac{6}{36}, & x=0 \\
\frac{10}{36}, & x=1 \\
\frac{8}{36}, & x=2 \\
\frac{6}{36}, & x=3 \\
\frac{4}{36}, & x=4 \\
\frac{2}{36}, & x=5
\end{matrix}\right\}=G_X(t)=\frac{1}{36}\left(6t^0 + 10t^1 + 8t^2 + 6t^3 + 4t^4 + 2t^5\right)$$
```

```ad-example
The probability generating function of the discrete random variable 𝑋 is given by $𝐺_𝑋 (𝑡)=𝑘(1+𝑡)^2$ (a) Find the value of 𝑘. (b) Write down the probability distribution of 𝑋.```

$$G_X(t)=k(1+2t+t^2)=k+2kt+kt^2$$
$$G_X(1)=1$$
$$\implies k+2k+k=4k=1 \implies k = \frac{1}{4}$$

$$G_X(t)=\frac14t^0+\frac12t^1+\frac14t^2$$

$$P(x)=\left\{\begin{matrix}
\frac{1}{4}, & x=0 \\
\frac{1}{2}, & x=1 \\
\frac{1}{4}, & x=2
\end{matrix}\right\}=G_X(t)=\frac14t^0+\frac12t^1+\frac14t^2$$
```

## Common Distributions

### Discrete Uniform Distribution
Consider
$$X\sim U(1,n)$$

This yields (**YOU SHOULD MEMORISE OR DERIVE THIS**)
$$G_X(t)=\frac1nt^1+\frac1nt^2+\frac1nt^3+\dots$$
$$=\frac1n\left(t^1+t^2+t^3+\dots\right)$$
$$=t\frac1n\left(t^0+t^1+t^2+\dots\right)$$
$$=\frac{t}{n}(S_n)=\frac{t}{n}\times\frac{1-t^n}{1-t}$$
$$=\frac{t(1-t^n)}{n(1-t)}$$

### Binomial Distribution
Consider
$$X\sim B(n,p)$$

This yields

$$G_X(t)= (q+pt)^n$$

**YOU SHOULD MEMORISE OR DERIVE THIS**

### Geometric Distribution
```ad-recall
A geometric distribution is the number of trials up to and including a successful trial.

The single parameter is the probability of each success.

$$P(X=x)=(1-p)^{x-1}\times p$$

$$P(X \leq x)=1-P(X \gt x)=1-(1-p)^x$$
```

Consider
$$X\sim \text{Ge}(p)$$

this yields
$$G_X(t)=pt^1+q^1pt^2+q^2pt^3\dots$$
$$a_n=pt(qt)^{n-1}\implies S_\infty=\frac{pt}{1-qt}$$
$$G_X(t)=\frac{pt}{1-qt}$$

**YOU SHOULD MEMORISE OR DERIVE THIS**

## Poisson Distribution
```ad-recall
The number of outcomes in a set period of time given a constant rate of occurrence, $\lambda$

$$P(X=x)=e^{-\lambda}\frac{\lambda^x}{x!}$$
```

Consider
$$X\sim \text{Po}(\lambda)$$

this yields
$$G_X(t)=e^{-\lambda}\left(\lambda^0 t^0+\frac{\lambda^1}{1}t^1+\frac{\lambda^2}{2}t^2+\dots\right)$$
by the Maclaurin expansion we can rewrite $G_X(t)$ as
$$G_X(t)=e^{-\lambda}e^{\lambda t}=e^{\lambda(t-1)}$$
# Calculating Statistical Moments ($E$ and $\text{Var}$)
## Calculating Expected Value
Consider a probability generating function
$$G_X(t)=\sum\left(p(x_i)\times t^{x_i}\right)$$
differentiating with respect to $t$,
$$G_X'(t)=\sum\left(x_ip(x_i)\times t^{x_i-1}\right)$$
substituting $t=1$ into $G_X'(t)$ yields
$$G_X'(1)=\sum x_i\times p(x_i)=E(X)$$
$$G_X'(1)=E(X)$$

## Calculating Variance
differentiating (again) with respect to $t$,
$$G_X''(t)=\sum\left(x_i(x_i-1)p(x_i)\times t^{x_i-2}\right)$$
$$=\sum\left(x_i^2p(x_i)-x_ip(x_i) \right)t^{x_i-2}$$
substituting $t=1$ into $G_X''(t)$ yields
$$=E(X^2)-E(X)$$
$$\text{Var}(X)=E(X^2)-E(X)+E(X)-E(X)^2$$
substitute,
$$\text{Var}(X)=G_X''(1)+G_X'(1)-G_X'(1)^2$$

```ad-example
The discrete random variable $𝑋$ has probability generating function given by $𝐺_𝑋 (𝑡)=\frac{1}{100000} (9+𝑡^2 )^5$. Find 

(a) 𝐸(𝑋) 
$$G_X'(t)=\frac{10t}{100000}(9+t^2)^4$$
$$G_X'(1)=\frac{1}{10000}(10)^4$$
$$G_X'(1)=\frac{1}{1}=1$$

(b) 𝑉𝑎𝑟(𝑋)
$$G_X''(t)=\frac{t}{10000}(9+t^2)^4$$
$$[(9+t^2)^4]'=8t(9+t^2)^3$$
$$\left[\frac{t}{10000}\right]'=\frac{1}{10000}$$
$$G_X''(t)=\frac{1}{10000}\left(8t^2(9+t^2)^3+(9+t^2)^4\right)$$
$$G_X''(t)=\frac{1}{10000}(9+t^2)^3\left(8t^2+(9+t^2)\right)$$
$$G_X''(t)=\frac{9}{10000}(9+t^2)^3\left(t^2+1\right)$$
$$G_X''(1)=\frac{9}{10000}(10)^3\left(2\right)$$
$$G_X''(1)=\frac{9}{5}$$
$$\text{Var}(X)=1.8+1-1^2=1.8$$
```

```ad-example
A discrete random variable 𝑋 has a probability generating function given by $𝐺_𝑋 (𝑡)=𝑎+𝑏𝑡+𝑐𝑡^2$ where 𝑎,𝑏,𝑐 are constants. Given that the expected value of 𝑋 is $\frac76$ and the variance is $\frac{29}{36}$, find the values of 𝑎,𝑏 and 𝑐.

$$E(X)=\frac76=G_X'(1)$$
$$\text{Var}(X)=G_X"(1)-\frac76+\frac{49}{36}=\frac{29}{36}$$
$$\implies G_X''(1)=\frac{11}{18}$$

$$b+2c=\frac76$$
$$2c=\frac{11}{18} \implies c = \frac{11}{36}$$
$$\implies b = \frac59$$
$$a+\frac{5}{9}+\frac{11}{36}=1$$
$$\implies a = \frac{5}{36}$$
```

# Sums of Random Variables
The probability distribution, $Z$, of the sum of two independent, discrete random variables, $X + Y$, has an associated probability generating function 

$$G_Z(t)=G_X(t)\times G_Y(t)$$

```ad-example
Two independent discrete random variables $𝑋$ and $𝑌$ have probability generating functions $𝐺_𝑋 (𝑡)=\frac12+\frac12 𝑡$ and $𝐺_𝑌 (𝑡)=\frac13+\frac12 𝑡+\frac16 𝑡^2$. 

(a) Find the probability generating function of the random variable $𝑍=𝑋+𝑌$. 

$$G_Z(t)=G_X(t)\times G_Y(t)$$
$$G_Z(t)=(\frac12+\frac12t)(\frac13+\frac12t+\frac16t^2)$$

$$=\frac16+\frac5{12}t+\frac13t^2+\frac1{12}t^3$$

(b) Use probability generating functions to show that $𝐸(𝑍)=𝐸(𝑋)+𝐸(𝑌)$

$$G_Z'(t)=\frac{5}{12}+\frac23t+\frac14t^2$$
$$G_Z'(1)=\frac43$$
$$G_X'(t)=\frac12$$
$$G_Y'(t)=\frac12+\frac13t$$
$$G_Y'(1)=\frac56$$
$$G_X'(1)+G_Y'(1)=\frac43$$
$$\implies E(Z)=E(X)+E(Y)$$
```

## Linear Coding of Random Variables

Consider $X$ with PGF $G_X(t)$. If $Y=aX+b$, then the PGF 

$$G_Y(t)=t^bG_X(t^a)$$

```ad-info
So here $a$ is multiplying the outcomes of $X$. The powers of $t$ should be equal to the outcomes, therefore the argument of the PGF $G_Y(t)$ should have $t^a$ as indeces have a law in which $({t^a})^\sigma=t^{a\sigma}$.

When $X=0$, the $b$ is the only thing that changes the outcome of $X$ for $Y$, therefore, the only way of changing the term containing the product $t^0$ to $t^b$ is by multiplying the PGF by $t^b$.
```

Consider $X$ such that $G_X(t)=\sum P(x_i) \times t^{x_i}$. 
$$\text{let}\space Y=aX+b$$
$$G_Y(t)=\sum P(ax_i+b) \times t^{ax_i+b}$$
$$G_Y(t)=\sum P(y_i) \times t^b \times (t^a)^{x_i}$$
$$P(y_i)=P(x_i)$$
$$G_Y(t)=t^b\sum P(x_i) (t^a)^{x_i}$$
$$=t^bG_X(t^a)$$


```ad-example
A random variable $𝑋$ has a probability generating function $𝐺_𝑋 (𝑡)=\frac23+\frac13 𝑡$. 

(a) Write down the probability distribution of $𝑋$.
$$P(X=x)=\left\{\begin{matrix}
\frac{2}{3}, & x=0 \\
\frac{1}{3}, & x=1
\end{matrix}\right\}$$

(b) $𝑌=2𝑋+1$. Write down the probability distribution of $𝑌$ and hence find the probability generating function of $𝑌$. 
$$P(Y=y)=\left\{\begin{matrix}
\frac{2}{3}, & y=1 \\
\frac{1}{3}, & y=3
\end{matrix}\right\}$$

$$G_Y(t)=\frac23t+\frac13t^3$$

(c) Verify that $𝐺_𝑌 (𝑡)=𝑡𝐺_𝑋 (𝑡^2 )$.
$$tG_X(t^2)=t(\frac23+\frac13t^2)=\frac23t+\frac13t^3$$
Verified.
```