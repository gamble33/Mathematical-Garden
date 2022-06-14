#Statistics #Maths 

# Poisson Distribution
The Poisson Distribution is a distribution over the number of events which occur within a period of time, given an average rate $\lambda$.

$$P(X=x)=\frac{e^{-\lambda}\lambda^x}{x!}$$
## Events Must Occur
* Singular in time.
* Independently of each other.
  At a constant rate in the sense that the mean number of occurences in the interval is proportional to the length of the interval.

## Approximating a Binomial using a Poisson
If
$$X \sim B(n,p)$$
and
- $n$ is large
- $p$ is small
Then $X$ can be approximated by $Po(np)$. Generally, if $np \leq 10$, then a Poisson is a suitable approximation, but in an exam, use the original Binomial unless instructed to approximate.
## Using a suitable approximation...
![[Pasted image 20220530095535.png]]