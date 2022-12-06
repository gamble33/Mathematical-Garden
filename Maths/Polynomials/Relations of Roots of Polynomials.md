#Polynomials #Maths 

# Relations of [[Roots of Polynomials|Roots]] of [[Polynomials]]
---
> [!Note]
> $\alpha$, $\beta$, $\gamma$, $\delta$ are used to represent the roots of a polynomial.

> [!Warning]
> Lookout for missing powers of $x$. A cubic polynomial may look as such $x^3 -x + 3 = 0$ where $a=1$, $b=0$, $c=-1$ and $d=3$.

- the sum of the roots $\alpha + \beta=-\frac{b}{a}$.
	- To generalize, the sum of roots $\sum{\alpha}=-\frac{b}{a}$.
- the product of the roots $\alpha\beta = \frac{c}{a}$.
	- More generally, the sum of possible product of roots $\sum{\alpha\beta}=\frac{c}{a}$.
- The sum of products of triples, $\sum{\alpha\beta\gamma}=-\frac{d}{a}$.

![[Pasted image 20220829123957.png]] #Todo draw table.

### Example Question
![[Pasted image 20220829130639.png]]
### Intuition
#### [[Quadratics|Quadratic]] polynomial
Consider a quadratic polynomial in the form 
$$ax^2+bx+c \equiv a(x-\alpha)(x-\beta)$$

Where:
$\alpha$ and $\beta$ are the roots of the polynomial.

By expanding $a(x-\alpha)(x-\beta)$,
$$a(x^2-\beta x - \alpha x + \alpha\beta)$$
$$ax^2-a\beta x - a\alpha x + a\alpha\beta$$
and refactoring
$$ax^2-a(\alpha+\beta)x + a\alpha\beta$$
this expression has been put into the form $ax^2 + bx + c$. Thus, we can equate the coefficients.
$$b=-a(\alpha+\beta)$$
$$\implies \alpha + \beta = -\frac{b}{a}$$
Also,
$$c=a\alpha\beta$$
$$\implies \alpha\beta=\frac{c}{a}$$


## A consequence of notation
As a result of the [[Notation#Sums of Roots of Polynomials Notation]], we derive the identity


## $S_{-1}$ Notation
$S_{-1}$ is the sum of the reciprocals of the roots. I.e., $\frac{1}{\alpha}+\frac{1}{\beta}+\frac{1}{\gamma}+\space...$

By equating the denominator of the fractions, the sum of the reciprocals can be put into the form $\frac{\alpha\beta + \beta\gamma + \alpha\gamma}{\alpha\beta\gamma}$. In this form, for a $n^{\text{th}}$ order polynomial the denominator will always be the product of $n$ roots. The numerator will be equal to the sum of all the possible $n-1$ tuples.

For cubic polynomials
$$S_{-1}=\frac{\sum{\alpha\beta}}{\sum{\alpha\beta\gamma}}=\frac{\frac{c}{a}}{-\frac{d}{a}}=-\frac{c}{d}$$
## $S_3$ Notation
#Todo
$$(S_1)^3=S_3+3\sum{\alpha}\sum{\alpha\beta}-3\sum{\alpha\beta\gamma}$$
This is true for all polynomials with an order higher than 3.

## Recurrence Formula
Say we have the polynomial $3x^3+2x^2-4x+1=0$.
$$S_1=-\frac{2}{3}$$
$$S_{-1}=4$$
$$\sum{\alpha\beta}=-\frac{4}{3}$$
$$\sum{\alpha\beta\gamma}=-\frac{1}{3}$$
By the [[Factor Theorem]], we know that if we substitute any of the roots ($\alpha$, $\beta$ or $\gamma$) then the result will be $0$.
$$3\alpha^3+2\alpha^2-4\alpha+1=0$$
$$3\beta^3+2\beta^2-4\beta+1=0$$
$$3\gamma^3+2\gamma^2-4\gamma+1=0$$
Therefore, if we were to sum each of these polynomial expressions, the result will still be $0$.

Thus, we can rewrite the sum of the polynomial expressions with $S$ notation
$$3S_3+2S_2-4S_1+3=0$$ 
## Summary
![[Pasted image 20220830153416.png]]
#Todo 
### Sums of Squares:
- Quadratic: $\alpha^2+\beta^2=(\alpha+\beta)^2-2\alpha\beta$

## Transforming Roots of Polynomials
**Example Question**
The cubic equation $f(x)=x^3-2x^2+4$ has roots $\alpha, \beta, \gamma$. Find the equation $g(w)$ with roots $(3\alpha-1)$, $(3\beta-1)$, $(3\gamma-1)$.

If we transform the roots by $\text{root}\times3 - 1$, then every point on $f(x)$ should be transformed by $3x-1$. Therefore, the new function, $g(w)$ should be equal to $f(3x-1)$.

$$w=3x-1$$
$$\therefore \space x=\frac{w+1}{3}$$
$$\implies f(x)=f\left(\frac{w+1}{3}\right)=\left(\frac{w+1}{3}\right)^3-2\left(\frac{w+1}{3}\right)^2+4$$
The cubic equation $f(x)=x^3-2x^2+4=0$ is expressible as $(x-\alpha)(x-\beta)(x-\gamma)$
$$(x-\alpha)(x-\beta)(x-\gamma)\equiv(3x-3\alpha)(3x-3\beta)(3x-3\gamma)$$
$$\equiv[(3x-1)-(3\alpha-1)][(3x-1)-(3\beta-1)][(3x-1)-(3\gamma-1)]$$
Let $w=3x-1\to x=\frac{w+1}{3}$
This makes it obvious that $w$ must equal $w=3x-1$.

### Example Question
Given that $x^3-3x^2+12=0$ has roots $\alpha$, $\beta$, $\gamma$, find
- $\alpha + \beta + \gamma$
$$S_1=-\frac{b}{a}=-\frac{-3}{1}=3$$
- $\alpha\beta + \alpha\gamma + \beta\gamma$
$$\sum{\alpha\beta}=\frac{c}{a}=\frac{0}{1}=0$$
- $\alpha^2+\beta^2+\gamma^2$
$$\frac{x^3}{x}-\frac{3x^2}{x}+\frac{12}{x}=0$$
$$x^2-3x+\frac{12}{x}=0$$
$$S_2-3S_1+12S_{-1}=0$$
$$S_2=3S_1+12S_{-1}$$
$$S_2=9-12\frac{c}{d}$$
$$S_2=9-12\frac{0}{12}=9$$
### Example Question
$x^3-x+7=0$
Find $\sum{\alpha}$ and $\sum{\alpha^2}$
$$\sum{\alpha}=S_1=-\frac{b}{a}=-\frac{0}{1}=0$$
$$x^2-1+\frac{7}{x}=0$$
$$S_2-3+7S_{-1}=0$$
$$S_2=3-7S_{-1}$$
$$S_{-1}=-\frac{c}{d}=\frac{1}{7}$$
$$\implies =S_2=3-\frac{7}{7}=2$$
### Example Question
$x^3+ax^2+bx+a=0$
Find $\sum{\alpha}$ and $\sum{\frac{1}{\alpha}}$
$$\sum{\alpha}=S_1=-\frac{a}{1}=-a$$
$$\sum{\frac{1}{\alpha}}=S_{-1}=-\frac{b}{a}$$
It is given that $\sum{\alpha}=\sum{\frac{1}{\alpha}}$
$$a=\frac{b}{a}\implies a^2=b$$ 
$$x^2+ax+b+\frac{a}{x}=0$$
$$S_2+aS_1+3b+aS_{-1}=0$$
$$S_2=-(-a^2+3b-b)$$
$$S_2=a^2-2b=a^2-2a^2$$
$$\implies S_2 < 0 \implies \{\alpha, \beta\} \in \mathbb{C}$$

### Example Question
A cubic polynomial is given by:
$$2x^3-x^2+x-5=0$$
With roots $\alpha$, $\beta$ and $\gamma$.
Find the value of $S_{-2}$