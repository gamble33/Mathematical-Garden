#Maths 

# Summation of [[Series]]
---
## Sum of ones
$$\sum^n_{r=1}{1}=n$$
### Derivation
$$\sum^n_{r=1}=\underbrace{(1+1+1+\dots+1)}_{n}=n$$
## The sum of the first $n$ [[Integer|integers]] ($\sum^n_{r=1}{r}$)
$$\sum^n_{r=1}{r}=\frac{1}{2}n(n+1)$$
### Derivation
$$A: 1+2+3+4+\dots+n$$
$$B:n+(n-1)+(n-2)+(n-3)+\dots+1$$

$A$ and $B$ are equal sums, they are just added in reversed order.
$$A+B: \underbrace{((n+1)+(n+1)+\dots+(n+1))}_{n}=n\times(n+1)$$
$$2A=n(n+1)\implies A=\frac{1}{2}n(n+1)$$
## The sum of the first $n$ squares ($\sum^n_{r=1}{r^2}$)
$$\sum^n_{r=1}{r^2}=\frac{1}{6}n(n+1)(2n+1)$$
### Derivation
Consider:
$$(r+1)^3=r^3+3r^2+3r+1$$
Sum both sides
$$\sum^n_{r=1}{(r+1)^3}$$
$$2^3=1^3+3\times1^2+3\times1+1$$
$$3^3=2^3+3\times2^2+3\times2+1$$
$$4^3=3^3+3\times3^2+3\times3+1$$
$$\vdots$$
$$(n+1)^3=n^3+3\times n^2+3\times n+1$$
$$2^3+^3+4^3+\dots+(n+1)^3=\sum^n_{r=1}{r^3}+3\sum^n_{r=1}{r^2}+3\sum^n_{r=1}{r}+\sum^n_{r=1}{1}$$
Notice the L.H.S. is just $\sum^n_{r=1}{r^3} - 1 + (n+1)^3$. Therefore we subtract $\sum^n_{r=1}{r^3}$ from both sides.
$$(n+1)^3-1=3\sum^n_{r=1}{r^2}+3\left[\frac{n(n+1)}{2}\right]+n$$
Rearrange and make $\sum^n_{r=1}{r^2}$ the subject.
$$3\sum^n_{r=1}{r^2}=n^3+3n^2+3n+1-1-n-\frac{3n(n+1)}{2}$$
$$3\sum^n_{r=1}{r^2}=n^3+3n^2+2n-\frac{3n(n+1)}{2}$$
$$6\sum^n_{r=1}{r^2}=2n^3+6n^2+4n-3n(n+1)$$
$$6\sum^n_{r=1}{r^2}=2n^3+6n^2+4n-3n^2-3n$$
$$6\sum^n_{r=1}{r^2}=2n^3+3n^2+n=n(2n^2+3n+1)$$
Factorize the [[Quadratic Functions|quadratic]].
$$2n^2+3n+1=(2n+1)(n+1)$$
$$\therefore\sum^n_{r=1}{r^2}=\frac{1}{6}n(2n+1)(n+1)$$
## The sum of the first $n$ cubes ($\sum^n_{r=1}{r^3}$)

$$\sum^n_{r=1}{n^3}=\frac{1}{4}n^2(n+1)^2$$
> [!Note]
> $$\sum^n_{r=1}{r^3}=\left(\sum^n_{r=1}{r}\right)^2$$

### Derivation
$$(r+1)^4=r^4+4r^3+6r^2+4r+1$$
Apply the same strategy as with the sum of squares. I.e., sum both sides to $n$.
$$2^4+3^4+4^4+\dots+(n+1)^4=\sum^n_{r=1}{n^4}+4\sum^n_{r=1}{n^3}+6\sum^n_{r=1}{n^2}+4\sum^n_{r=1}{n}+\sum^n_{r=1}{n}$$
$$\sum^n_{r=1}{n^4}-1+(n+1)^4=\sum^n_{r=1}{n^4}+4\sum^n_{r=1}{n^3}+6\sum^n_{r=1}{n^2}+4\sum^n_{r=1}{n}+\sum^n_{r=1}{n}$$
Subtract $\sum^n_{r=1}{n^4}$ from both sides and rearrange.
$$\vdots$$
$$\sum^n_{r=1}{n^3}=\frac{1}{4}n^2(n+1)^2$$
## Breaking down more complex sums
Summation is a [[Linear Function|linear function]]. Meaning [[Scalar|scalars]] can be factored out. I.e., 
$$\sum^n_{r=1}{kr}=k\sum^n_{r=1}{r}$$
**Quick Proof.**
$$\sum^n_{r=1}{kr}=k+2k+\dots+nk=k(1+2+\dots+n)=k$$
Summation is distributive over addition
$$\sum^n_{r=1}{(a_r+b_r)}=a_1+b_1+a_2+b_2+\dots+a_n+b_n$$
$$=a_1+a_2+\dots+a_n+b_1+b_2+\dots+b_n$$
$$=\sum^n_{r=1}{a_i}+\sum^n_{r=1}{b_i}$$

## Dealing with other bounds
## Method of differences
### General Form
If we have a sequence, $u_n$ which is expressible as the difference of consecutive terms of a function. 
$$u_n=f(n)-f(n+1)$$
Then the summation of the sequence $u_n$ will be: 
$$\sum^n_{r=1}{u_r}=f(1) - f(n + 1)$$
### Exploration Example
$$\sum^n_{r=1}{\frac{1}{r}-\frac{1}{r+1}}$$
$$=\frac{1}{1}-\left(\frac{1}{2}+\frac{1}{2}\right)-\left(\frac{1}{3}+\frac{1}{3}\right)-\frac{1}{4}+\dots+\frac{1}{n}-\frac{1}{n+1}$$
Cancellation,
$$=1-\frac{1}{n+1}=\frac{n}{n+1}$$
$$\implies \sum^\infty_{r=1}\frac{1}{r(r+1)}=1$$
### Proof Example
It is given that $4r^3=r^2(r+1)^2-(r-1)^2r^2$.
Prove that:
$$\sum^n_{r=1}{r^3}=\frac{1}{4}n^2(n+1)^2$$
$$\sum^n_{r=1}{r^2(r+1)^2-(r-1)^2r^2}=({\color{teal}1^2 2^2} - 0^2 1^2)+({\color{pink}2^2 3^2} - {\color{teal}1^2 2^2}) + (3^2 4^2 - {\color{pink}2^2 3^2}) + \dots + n^2(n+1)^2 - (n-1)^2n^2$$
$$=n^2(n+1)^2$$
Therefore,
$$4\sum^n_{r=1}{r^3}=n^2(n+1)^2$$
$$\sum^n_{r=1}{r^3}=\frac{1}{4}n^2(n+1)^2$$

### Partial Fractions Example
$$\sum^n_{r=1}\frac{1}{4r^2-1}$$
$$=\sum^n_{r=1}{\frac{1}{2(2r-1)}-\frac{1}{2(2r+1)}}$$
$$=\frac{1}{2}\sum^n_{r=1}{\frac{1}{(2r-1)}-\frac{1}{(2r+1)}}$$
$$=\frac{1}{2}\left( \frac{1}{1}-\frac{1}{3}   + \frac{1}{3} - \frac{1}{5} + \frac{1}{5} - \frac{1}{7} + \dots + \frac{1}{2n-1} - \frac{1}{2n+1}\right)$$
$$\vdots$$
$$=\frac{n}{2n+1}$$
### Non-consecutive Differences
Example:
$$u_r = f(r)-f(r+2)$$
$$\sum^n_{r=1}{\frac{1}{r}-\frac{1}{r+2}}$$
$$=\frac{1}{1}-{\color{orange}\frac{1}{3}}+\frac{1}{2}-{\color{lightgreen}\frac{1}{4}}+{\color{orange}\frac{1}{3}}-\frac{1}{5}+{\color{lightgreen}\frac{1}{4}}-\frac{1}{6}+\dots+\frac{1}{n-1}-\frac{1}{n+1}+\frac{1}{n}-\frac{1}{n+2}$$
$\frac{1}{1}$ and $\frac{1}{2}$ are the two terms that wont cancel at the start of the summation. By symmetry, we know that $-\frac{1}{n+1}$ and $-\frac{1}{n+2}$.
$$\vdots$$
$$=\frac{n(3n+5)}{2(n+1)(n+2)}$$