#Maths 

# Proof by Induction
---
## Overview
Step 1, Basis:
Prove the general statement is true for $n=1$

Step 2, Assumption:
Assume the general statement is true for $n=k$

Step 3, Inductive:
Show that the general statement is then true for $n=k+1$

Step 4, Conclusion: The general statement is then true for all positive integers $n$.

## Summation Proofs
**Example 1**

Show that 
$$\sum\limits^n_{r=1}(2r-1)=n^2$$
for all $n\in\mathbb{N}$.

Basis:
For $n=1$.
$$\sum\limits^1_{r=1}(2r-1)=\text{LHS}$$
$$2(1)-1=\text{LHS}$$
$$1=\text{LHS}$$

$$\text{RHS}=1^2$$
$$\text{RHS}=1$$
$$\space$$
$$\text{LHS}=\text{RHS}$$

Assumption:
Assume for $n=k$,
$$\sum\limits^k_{r=1}(2r-1)=k^2$$

Induction:
let $n=k+1$.
$$\sum\limits^{k+1}_{r=1}(2r-1)=\text{LHS},\space\text{RHS}=(k+1)^2$$
$$\sum\limits^{k}_{r=1}(2r-1)+[2(k+1)-1]=\text{LHS}$$
$$k^2+[2(k+1)-1]=\text{LHS}$$
$$k^2+[2k+2-1]=\text{LHS}$$
$$k^2+2k+1=\text{LHS}$$
by perfect square
$$(k+1)^2=\text{LHS}$$

Conclusion:

Since the statement is true for $n=1$ and if it is true for $n=k$, then it is true for $n=k+1$, therefore, it is true for all $n$ greater than 1.

**Example 2**

Prove by induction that for all positive integers $n$,
$$\sum\limits^n_{r=1}{2^rr}=2(1+(n-1)2^n)$$

Basis: For $n=1$,
$$\sum\limits^1_{r=1}{2^{r}r}=\text{LHS},\space \text{RHS}=2(1+(1-1)2^1)$$
$$2^1\times1=\text{LHS}$$
$$2=\text{LHS}$$
$$\text{RHS}=2(1+(1-1)2^1)$$
$$\text{RHS}=2(1+(0)2^1)$$
$$\text{RHS}=2(1)$$
$$\text{RHS}=2$$
$$\space$$
$$\text{LHS}=\text{RHS}$$

Assumption: Assume true for $n=k$,
$$\sum\limits^k_{r=1}{2^rr}=2(1+(k-1)2^k)$$

Induction: let $n=k+1$.
$$\sum\limits^{k+1}_{r=1}{2^rr}=\text{LHS},\space\text{RHS}=2(1+({k+1}-1)2^{k+1})$$
$$\sum\limits^k_{r=1}{2^rr}+2^{k+1}(k+1)=\text{LHS}$$
$$2(1+(k-1)2^k)+2^{k+1}(k+1)=\text{LHS}$$
$$2(1+(k-1)2^k+2^k(k+1))=\text{LHS}$$
$$2[1+2^k(k-1+k+1)]=\text{LHS}$$
$$2[1+2^k(2k)]=\text{LHS}$$
$$2[1+2^{k+1}k]=\text{LHS}$$
$$2[1+2^{k+1}(k+1-1)]=\text{LHS}$$
$$2[1+(k+1-1)2^{k+1}]=\text{LHS}$$
$$\space$$
$$\text{LHS}=\text{RHS}$$

Conclusion:

Since the statement is true for $n=1$ and if it is true for $n=k$, then it is true for $n=k+1$, therefore, it is true for all $n$ greater than 1.

## Divisibility Proofs

**Example 1**

Prove by induction that $3^{2n}+11$ is divisible by $4$ for all positive integers $n$.

Basis: let $n=1$
$$3^{2(1)}+11=20$$
$$20=4\times5$$

Assumption: assume true for $n=k$
$$3^{2k}+11 \equiv 4\times a,\space a\in\mathbb{N}$$

Induction: consider $n=k+1$
$$\text{LHS}: 3^{2(k+1)}+11$$
$$=3^{2k+2}+11$$
$$=3^{2k}\times3^2+11$$
$$=3^{2k}\times9+11$$
> [!Tip]
> Split up multiples of the substituted part.

$$=3^{2k}\times8+3^{2k}+11$$
$$=3^{2k}\times8+4a$$
$$=4\times(3^{2k}\times2+a)$$

Conclusion:

Since the statement is true for $n=1$ and if it is true for $n=k$, then it is true for $n=k+1$, therefore, it is true for all $n$ greater than 1.

**Example 2**
Prove by induction that $8^n-3^n$ is divisible by $5$

Basis: let $n=1$
$$8^1-3^1=5\times1$$

Assumption: assume true for all $n=k$
$$8^k-3^k=5\times a$$
$$a\in\mathbb{N}, \forall k\in\mathbb{N}$$

Induction: consider $n=k+1$
$$8^{k+1}-3^{k+1}$$
$$=8^{k}\times8-3^{k}\times3$$
$$=8^{k}\times5-3^{k}\times0+3(8^k-3^k)$$
$$=8^{k}\times5+3(8^k-3^k)$$
$$=5\times8^k+3(5a)$$
$$=5\times8^k+15a$$
$$=5\times(8^k+3a)$$

Conclusion:

Since the statement is true for $n=1$ and if it is true for $n=k$, then it is true for $n=k+1$, therefore, it is true for all $n$ greater than 1.

## Matrix Proofs

**Example 1**
Prove by induction that $\left[\begin{matrix}1&-1\\0&2\end{matrix}\right]^n=\left[\begin{matrix}1&1-2^n\\0&2^n\end{matrix}\right]$ for all $n\in\mathbb{Z}^+$.

Basis: let $n=1$

$$\text{LHS}:\left[\begin{matrix}1&-1\\0&2\end{matrix}\right]^1=\left[\begin{matrix}1&-1\\0&2\end{matrix}\right]$$
$$\text{RHS}:\left[\begin{matrix}1&1-2^1\\0&2^1\end{matrix}\right]=\left[\begin{matrix}1&-1\\0&2\end{matrix}\right]$$
$$\text{LHS}=\text{RHS}$$

Assumption: assume true for all $n=k$
$$\left[\begin{matrix}1&-1\\0&2\end{matrix}\right]^k\equiv\left[\begin{matrix}1&1-2^k\\0&2^k\end{matrix}\right]$$

Induction: consider $n=k+1$
$$\text{LHS}:\left[\begin{matrix}1&-1\\0&2\end{matrix}\right]^{k+1}=\left[\begin{matrix}1&-1\\0&2\end{matrix}\right]^k\times\left[\begin{matrix}1&-1\\0&2\end{matrix}\right]$$
$$=\left[\begin{matrix}1&1-2^k\\0&2^k\end{matrix}\right]\times\left[\begin{matrix}1&-1\\0&2\end{matrix}\right]=\left[\begin{matrix}1&-1+2-2\times2^{k}\\0&2\times2^k\end{matrix}\right]$$
$$=\left[\begin{matrix}1&1-2^{k+1}\\0&2^{k+1}\end{matrix}\right]$$

$$\text{RHS}:\left[\begin{matrix}1&1-2^{k+1}\\0&2^{k+1}\end{matrix}\right]$$
$$\text{LHS}=\text{RHS}$$

> [!Tip]
> Separate the power. All matrix problems in Proof by Induction in A-level Further Maths will look like this *(Dated 2022, Cambridge Syllabus)*.

Conclusion:

Since the statement is true for $n=1$ and if it is true for $n=k$, then it is true for $n=k+1$, therefore, it is true for all $n$ greater than 1.

**Example 2**

Prove by induction that $\left[\begin{matrix}-2&9\\-1&4\end{matrix}\right]^n=\left[\begin{matrix}-3n+1&9n\\-n&3n+1\end{matrix}\right]$, $\forall n\in\mathbb{Z}^+$.

Basis: let $n=1$
$$\left[\begin{matrix}-2&9\\-1&4\end{matrix}\right]^1=\left[\begin{matrix}-3(1)+1&9(1)\\-(1)&3(1)+1\end{matrix}\right]=\left[\begin{matrix}-2&9\\-1&4\end{matrix}\right]$$

Assumption: assume true for all $n=k$
$$\left[\begin{matrix}-2&9\\-1&4\end{matrix}\right]^k\equiv\left[\begin{matrix}-3k+1&9k\\-k&3k+1\end{matrix}\right]$$

Induction: consider $n=k+1$
$$\text{LHS}:\left[\begin{matrix}-2&9\\-1&4\end{matrix}\right]^{k+1}=\left[\begin{matrix}-2&9\\-1&4\end{matrix}\right]^k\times\left[\begin{matrix}-2&9\\-1&4\end{matrix}\right]$$
$$=\left[\begin{matrix}-3k+1&9k\\-k&3k+1\end{matrix}\right]\times\left[\begin{matrix}-2&9\\-1&4\end{matrix}\right]$$
$$=\left[\begin{matrix}6k-2-9k&-27k+9+36k\\2k-3k-1&-9k+12k+4\end{matrix}\right]$$
$$=\left[\begin{matrix}-3k-2&9k+9\\-k-1&3k+4\end{matrix}\right]$$
$$=\left[\begin{matrix}-3(k+1)+1&9(k+1)\\-(k+1)&3(k+1)+1\end{matrix}\right]$$

Conclusion:

Since the statement is true for $n=1$ and if it is true for $n=k$, then it is true for $n=k+1$, therefore, it is true for all $n$ greater than 1.

## Sequence Proofs
**Example 1**
A recurrence relationship is $u_{n+1}=u_n+2n+2,u_1=1$.

Prove that the $n^{\text{th}}$ term is $u_n=n^2+n-1$.

Basis: let $n=1$
$$u_1=1^2+1-1=2-1=1$$
let $n=2$,
$$u_2=2^2+2-1=5$$
$$u_2=u_1+2(1)+2=1+2+2=5$$

> [!Warning]
> Our basis should include all initial instances for the first recurrence.

Assumption: assume true for all $n=k$
$$u_k=k^2+k-1$$

Induction: consider $n=k+1$
> [!Tip]
> Define $u_{k+1}$ using the recurrence relationship.

$$u_{k+1}=u_k+2k+2$$
$$=(k^2+k-1)+2k+2$$
$$=k^2+3k+1$$
$$=k^2+2k+k+1$$
$$=(k^2+2k+1)+(k+1)-1$$
$$=(k+1)^2+(k+1)-1$$
If it's true for $k$, it is true for $k+1$.

Conclusion:
 
Since the statement is true for $n=1$ and if it is true for $n=k$, then it is true for $n=k+1$, therefore, it is true for all $n$ greater than 1.

**Example 2**
For the [[Fibonacci]] numbers $F_1=1$, $F_2=1$, $F_3=2$, $F_4=3$, $F_5=5$, $F_6=8$, $F_7=13$, $F_8=21$, $F_9=34$, $F_{10}=55$, Prove that $F_n=\frac{(1+\sqrt{5})^n-(1-\sqrt{5})^n}{2^n\times\sqrt{5}}$.

> [!Tip]
> Make the recurrence clear.
> $$F_{n+2}=F_{n+1}+F_n$$

Basis: let $n=1$
> [!Note]
> Since the recurrence relationship depends on the previous two terms, the first three terms must be demonstrated as the basis of the proof.

$$F_1=\frac{(1+\sqrt{5})^1-(1-\sqrt{5})^1}{2^1\times\sqrt{5}}$$
$$F_1=\frac{2\sqrt{5}}{2\sqrt{5}}=1$$

$$\space$$

$$F_2=\frac{(1+\sqrt{5})^2-(1-\sqrt{5})^2}{2^2\times\sqrt{5}}$$
$$F_2=\frac{(2)(2\sqrt{5})}{4\sqrt{5}}=1$$
$$F_2=\frac{4\sqrt{5}}{4\sqrt{5}}=1$$

$$\space$$

$$F_3=\frac{(1+\sqrt{5})^3-(1-\sqrt{5})^3}{2^3\times\sqrt{5}}$$
By the [[Difference of Two Powers]]:
$$F_3=\frac{(2\sqrt{5})((1+\sqrt{5})^2+(1+\sqrt{5})(1-\sqrt{5}))+(1-\sqrt{5})^2)}{2^3\times\sqrt{5}}$$
$$F_3=\frac{(1+\sqrt{5})^2+(1+\sqrt{5})(1-\sqrt{5}))+(1-\sqrt{5})^2}{2^2}$$
$$\vdots$$
$$F_3=\frac{8}{4}=2$$

Assumption: assume true for all $n=k$ and $n=k-1$
$$F_k\equiv\frac{(1+\sqrt{5})^k-(1-\sqrt{5})^k}{2^k\times\sqrt{5}}$$
$$F_{k-1}\equiv\frac{(1+\sqrt{5})^{k-1}-(1-\sqrt{5})^{k-1}}{2^{k-1}\times\sqrt{5}}$$

Induction: consider $n=k+1$
$$F_{k+1}=F_k+F_{k-1}$$
$$=\frac{(1+\sqrt{5})^k-(1-\sqrt{5})^k}{2^k\times\sqrt{5}}+\frac{(1+\sqrt{5})^{k-1}-(1-\sqrt{5})^{k-1}}{2^{k-1}\times\sqrt{5}}$$
$$=\frac{\frac{1}{2}\left[(1+\sqrt{5})^k-(1-\sqrt{5})^k\right]}{2^{k-1}\times\sqrt{5}}+\frac{(1+\sqrt{5})^{k-1}-(1-\sqrt{5})^{k-1}}{2^{k-1}\times\sqrt{5}}$$
$$=\frac{\frac{1}{2}(1+\sqrt{5})^k-\frac{1}{2}(1-\sqrt{5})^k+(1+\sqrt{5})^{k-1}-(1-\sqrt{5})^{k-1}}{2^{k-1}\times\sqrt{5}}$$
$$=\frac{2(1+\sqrt{5})^k-2(1-\sqrt{5})^k+4(1+\sqrt{5})^{k-1}-4(1-\sqrt{5})^{k-1}}{2^{k+1}\times\sqrt{5}}$$
$$=\frac{\left(2+\frac{4}{1+\sqrt{5}}\right)(1+\sqrt{5})^k-(1-\sqrt{5})^k\left(2+\frac{4}{1-\sqrt{5}}\right)}{2^{k+1}\times\sqrt{5}}$$
$$=\frac{\left(1+\sqrt{5}\right)(1+\sqrt{5})^k-(1-\sqrt{5})^k\left(1-\sqrt{5}\right)}{2^{k+1}\times\sqrt{5}}$$
$$=\frac{(1+\sqrt{5})^{k+1}-(1-\sqrt{5})^{k+1}}{2^{k+1}\times\sqrt{5}}$$

Conclusion:
 
Since the statement is true for $n=1$, $n=2$ and $n=3$ and if it is true for $n=k$ and $n=k-1$, then it is true for $n=k+1$, therefore, it is true for all $n$ greater than 1.