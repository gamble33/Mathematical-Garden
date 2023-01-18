> [!Note]
> * All functions will be positive.
> * All counting starts at one.

# Comparison Test
Consider two series,
$$A=\sum^\infty_{k=1}a_k$$
$$B=\sum^\infty_{k=1}b_k$$

with $0 < a_k \leq b_k$ for all $k$.

It follows that:
$$a_1 \leq b_1$$
$$a_1 + a_2 \leq b_1 + b_2$$
$$a_1 + a_2 + a_3 \leq b_1 + b_2 + b_3$$
$$\vdots$$
$$\sum^\infty_{k=1}a_k \leq\sum^\infty_{k=1}b_k$$

It holds that if $A$ is divergent, then $B$ must also be divergent.

Likewise, if $B$ is convergent, then $A$ must also be convergent.

> [!Note]
> This is true because of the fact that $a_k$ and $b_k$ are both strictly greater than $0$. Otherwise, $A$ could diverge to $-\infty$ whilst $B$ converged to something else.

## Proof

Consider a sequence of partial sums $S_n$.
$$\{S_n\}=\left\{\sum^n_{k=1}x_k,\ \forall n \in \mathbb{N} \right\}$$ 

The partial sums are:
$$(x_1) \lt (x_1 + x_2) \lt (x_1 + x_2 + x_3) \lt \dots$$
Increasing.

Suppose that the series $\sum^\infty_{k=1}b_k$ converges. 
$$\sum^n_{k=1}a_k \leq\sum^n_{k=1}b_k \lt \sum^\infty_{k=1}b_k=\text{const}$$

The partial sum of $A$ is therefore, bounded above. Since $a_k \gt 0$, the partial sum of $A$ is an increasing function. Therefore, if it is increasing and bounded above, it must converge.

Alternatively, suppose $A$ diverges. Therefore, the sequence $\{S_n\}=\left\{\sum^n_{k=1}b_k\right\}$ is increasing and bounded below.

## Testing
> [!Example]
> Consider the sequences $a_k=\frac 1 {n^2}$ and $b_k = \frac {e^{-n}} {n^2}$
> $$0 < e^{-n} < 1$$
> $$\frac {1} {n^2} > e^{-n} \times \frac {1} {n^2}$$
> $$1>e^{-n}$$
> $$a_k > b_k > 0$$
> We are given that $A$ converges, therefore by the comparison test, $B$ must also converge.

## Hard Part
> [!Warning]
> The hard part is finding another sequence that would be suitable to use with the comparison test. 

> [!Example]
> Consider:
> $$a_k = \frac {1} {3^n + 1}$$
> Let's consider the sequence $b_k=\frac{1}{3^n}=1\times\left(\frac13\right)^n$
> 
> > [!Tip]
> > $b_k$, in this case, was chosen because it is a geometric sequence (thus it can be determined if it converges $|r|<1$) and is similar to $a_k$, that is, $b_k$ can easily be compared to $a_k$.
> 
> The infinite sum of $b_k$ converges to $\frac32$.
> 
> $$\frac{1}{3^n}>\frac1{3^n+1}$$
> $$b_k>a_k$$
> 
> thus, $A_n$ is increasing and is bounded above, thus it is also convergent.

> [!Example]
> Consider:
> $$a_k = \frac {1} {n^4 + e^n}$$
> > [!Note]
> > $\frac {1} {n^4}$ is also a valid candidate for $b_k$.
> > This is because it is considered *known* that reciprocal polynomials converge if the order is strictly greater than 1.
> 
> $$b_k=\left(\frac 1 e\right)^n$$
> $b_k$ converges to $\frac e {e - 1}$.
> 
> $$\frac {1} {n^4 + e^n}<\frac 1 {e^n}$$
> $$0 < a_k < b_k$$
> 
> $A_n$ is increasing and is bounded above, thus it is also convergent.

Consider:
$$a_k = \frac{1}{\ln n}$$
$$b_k=\frac 1 n$$

$$n>\ln n$$
$$e^n > n$$

therefore,

$$\frac 1 {\ln n} > \frac 1 n$$
$$a_k > b_k > 0$$

thus, $A_n$ is increasing and is bounded below $B_\infty$ and is therefore also divergent.

# Limit Comparison Test
Consider two series
$$A=\sum^\infty_{k=1}a_k$$
$$B=\sum^\infty_{k=1}b_k$$
$$a_k>0,\ b_k>0$$
$$if\ 0<\lim_{n\to\infty}\frac{a_n}{b_n}\lt\infty$$
$$\text{then}\ \sum^\infty_{k=1}a_k\ \text{and}\ \sum^\infty_{k=1}b_k$$
are either both convergent or both divergent.

# Integral Test
Consider a sequence $a_k,\ \text{where}\  a_k>0$

Consider a positive, continuous, and decreasing function $y=a(x)$ where $a(n)=a_n$, $\forall\  n \in \mathbb{N}$

![[Pasted image 20221214112422.png]]

$$\int\limits^\infty_1 a(x)\ dx \leq \sum^\infty_{k=1}a_k$$

therefore, if the integral is infinite, the series must diverge.

However,
![[Pasted image 20221214113318.png]]
$$\int\limits^\infty_1 a(x-1)\ dx \geq \sum^\infty_{k=1}a_k$$
therefore, if the integral converges, the series must also converge.

The same inequality can be obtained by starting the count from $k=2$:

$$\int\limits^\infty_1 a(x)\ dx \geq \sum^\infty_{k=2}a_k$$

if $\int\limits^\infty_1 a(x)\ dx$ is finite, then the series $\sum^\infty_{k=2}a_k$ is bounded above. Also $\sum^\infty_{k=2}a_k$ is increasing, therefore, $\sum^\infty_{k=2}a_k$ must be convergent.

If $a_1$ is constant, then $a_1 + \sum^\infty_{k=2}a_k = \sum^\infty_{k=1}a_k$ must also be convergent.

> [!Summary]
> * If the integral converges, then so does the series.
> * If the integral diveres, then so does the series.

> [!Example]
> Use the integral test to determine whether the series, $\sum^\infty_{n=1}\frac{1}{\sqrt[5]{n}}$, is convergent or divergent. 
> $$\int\limits^\infty_1 n^{-\frac15}\ dn \leq \sum^\infty_{n=1}\frac{1}{\sqrt[5]{n}}$$
> 
> $$\int\limits^\infty_1 n^{-\frac15}\ dn=\left[\frac54 n^{\frac45}\right]^\infty_1$$
> This is divergent, therefore the series is also divergent.

> [!Example]
> Use the integral test to determine whether the series, $\sum^\infty_{n=2}\frac{1}{n(\ln n)^2}$, is convergent or divergent. 
> $$\int\limits^\infty_2 \frac{1}{n(\ln n)^2}\ dn \geq \sum^\infty_{n=3}\frac{1}{n(\ln n)^2}$$
> $$\lim_{k\to\infty}\left(\left[-(\ln n)^{-1}\right]^k_2\right)=\frac{1}{\ln 2}$$
> The series from $n=3$ to $\infty$ converges.
> 
> $\frac{1}{2(\ln 2)^2}$ is finite and $\frac{1}{2(\ln 2)^2} + \sum^\infty_{n=3}\frac{1}{n(\ln n)^2}=\sum^\infty_{n=2}\frac{1}{n(\ln n)^2}$, therefore
> 
> $$\sum^\infty_{n=2}\frac{1}{n(\ln n)^2}\ \text{must converge.}$$

## Proof
Prove
$$\sum^\infty_1 n^T \lt \infty,$$
$$\ \forall\ T \lt -1$$

Consider:
$$\int\limits^\infty_1 n^T \ dn=\left[\frac{1}{T+1}n^{T+1}\right]^\infty_1$$
$$=\lim_{n=\infty}\left[\frac{1}{T+1}n^{T+1}\right]-\frac{1}{T+1}$$
for values of $T+1\lt 0$
$$\lim_{n=\infty}\left[\frac{1}{T+1}\times\frac{1}{n^{-(T+1)}}\right]-\frac{1}{T+1}=-\frac{1}{T+1}$$
the value of $-\frac{1}{T+1}$ is finite, therefore 
$\sum^\infty_1 n^T$ is increasing and bounded above, thus, it is convergent $\forall\ T \lt -1$.