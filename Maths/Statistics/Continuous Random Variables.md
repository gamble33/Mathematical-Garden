# Definitions
A **continuous random variable** is a statistical variable which is the output of an event that is continuous.

A **cumulative distribtion function** will yield the probability of the CRV being less than a specified value.

A **discrete random variable** is a statistical variable which is the output of an event that is discrete.

A **probability density function** is a function which can be interpreted as the relative likelihood of any outcome. To convert this to a probability, the area under the curve would need to be found

A **probability mass function** details the probability for any given outcome. 

An **$x$-centile** tells you the value of a data-set located at the $x\%$ point in the data.

The *$50^{\text{th}}$ percentile* is more commonly called the **median**

The *$25^{\text{th}}$ percentile* is more commonly called the **$1^{\text{st}}$ quartile**.

A **skew** is a measurement of the asymmetry of data. For a positive skew, $\text{mode}<\text{median}<\text{mean}$.

> [!Warning]
> **Unnecessary detail**
> 
> A measurement of skew:
> $$\mu_3=E\left[\left(\frac{x-\mu}{\sigma}\right)^3\right]$$

> [!Note]
> We should point out though, that a PMF is only associated with a DRV and a PDF is only associated with a CRV.

# Axioms
**If $X$ is a CRV with a PDF of $f(x)$, then we have these three properties:**

* $$f(x) \geq 0$$
* $$P(a \leq X \leq b) = \int\limits^b_a f(x)\ dx$$
* $$\int\limits^b_a f(x)\ dx = 1$$

**If $X$ is a CRV with CDF $F(x)$ **
* $$F(x)=P(X\leq x)=\int\limits^x_{-\infty}f(t)\ dt$$
	* The CDF is simply the integral of the PDF.
* $$f(x) = \frac{d[F(x)]}{dx}$$

> [!EXAMPLE]
> Given that $f(x)$ is a probability density function, find $k$.
> $$f(x)=\left \{\begin{matrix}|k(1-x^2)|, & 0\leq x \leq 2\ \\ 0 & \text{otherwise} \end{matrix}\right\}$$
> $$\int\limits^2_0|k(1-x^2)|\ dx=|k|\int\limits^2_0|(1-x^2)|\ dx$$
> $$=|k|\int\limits^1_0(1-x^2)\ dx-|k|\int\limits^2_1(1-x^2)\ dx$$
> $$=|k|\left([x-\frac13 x^3]^1_0-[x-\frac13 x^3]^2_1\right)$$
> $$=|k|\left(\frac23-2+\frac83-1+\frac13\right)$$
> $$=\frac23|k|=1$$
> $$k=1.5$$

> [!Example]
> The random variable $X$ has probability density function:
> $$f(x)=\left\{\begin{matrix}\frac25 x + \frac25, & 1 \leq x \leq 2 \\ 0 & \text{otherwise}\end{matrix}\right\}$$
> Find $F(x)$.
>
> $$\frac25\int (x+1)\ dx=\frac15x^2+\frac25x+C$$
> $$C=-\frac35$$
> $$F(x)=\left\{\begin{matrix}0&x\lt1\\\frac15x^2+\frac25x-\frac35, & 1 \leq x \leq 2 \\ 1 & 2\lt x \end{matrix}\right\}$$

# Measures of Location & Spread
## Expected Value ($\mu$)
**Discrete Random Variable**
$$E(X)=\sum^n_{i=0}x_i\times P(X=x_i)$$

**Continuous Random Variable**
$$E(X)=\int\limits^\infty_{-\infty} xf(x)\ dx$$

## Variance
**Discrete Random Variable**
$$\text{Var}(X)=E(X^2)-E(X)^2$$
$$\text{Var}(X)=\sum^n_{i=0}x^2_i\times P(X=x_i)-\mu^2$$

> [!Warning]
> This is a variance formula from a data-set.
> $$\text{Var}(X)=\frac{\sum (\mu - x)^2}{n}$$
> $$=\frac{\sum (\mu^2 - 2\mu x + x^2)}{n}=\frac{n\mu^2-2\mu \sum x + \sum x^2}{n}$$
> $$=E(X^2)-\mu^2$$

**Continuous Random Variable**
$$\text{Var}(X)=E(X^2)-E(X)^2$$
$$\text{Var}(X)=\int\limits^\infty_{-\infty} x^2f(x)\ dx-\mu^2$$

## Coding
$$E(aX+b)=a\mu+b$$
\
$$\text{Var}(aX+b)=E([aX+b]^2)-E(aX+b)^2$$
$$=E(a^2X^2+2aXb+b^2)-(aE(X)+b)^2$$
$$=E(a^2X^2)+E(2aXb)+E(b^2)-a^2E(X)^2-2abE(X)-b^2$$
$b^2$ is a constant, so $E(b^2)=b^2$.
$$=E(a^2X^2)+E(2aXb)-a^2E(X)^2-2abE(X)$$
$$=a^2E(X^2)+2abE(X)-a^2E(X)^2-2abE(X)$$
$$=a^2E(X^2)-a^2E(X)^2$$
$$=a^2\left[E(X^2)-E(X)^2\right]$$
$$\implies \text{Var}(aX+b)=a^2\times\text{Var}(X)$$

> [!Example]
> The random variable $X$ has probability density function
> $$f(x)=\left\{\begin{matrix}\frac14x, & 1 \leq x \leq 3 \\ 0 & \text{otherwise} \end{matrix}\right\}$$
> Find $E(X)$, $\text{Var}(X)$, $E(2X-3)$, and $\text{Var}(2X-3)$.
> $$E(X)=\int\limits^3_1x\times\frac14x\ dx=\frac14\int\limits^3_1x^2\ dx$$
> $$=\frac14\left[\frac13x^3\right]^3_1=\frac94-\frac1{12}=\frac{13}6$$
> \
> $$\text{Var}(X)=\frac14\int\limits^3_{1} x^3\ dx-\left(\frac{13}{6}\right)^2$$
> $$=\frac{1}{16}\left[x^4\right]^3_1-\frac{13^2}{36}=5-\frac{13^2}{36}=\frac{11}{36}$$
> \
> $$E(2X-3)=2E(X)-3=\frac43$$
> \
> $$\text{Var}(2X-3)=4\times\text{Var}(X)=\frac{11}9$$

> [!Example]
> The random variable $X$ has probability density function
> $$f(x)=\left\{\begin{matrix}\frac2{15}x, & 0 \leq x \lt 3 \\ \frac15(5-x) & 3 \leq x \leq 5 \\ 0 & \text{otherwise}\end{matrix}\right\}$$
> Find $E(X)$ and $\text{Var}(X)$.
> \
> $$E(X)=\int\limits^3_0\frac2{15}x^2\ dx + \int\limits^5_3\frac15(5x-x^2)\ dx$$
> $$=\frac83$$
> $$\text{Var}(X)=\int\limits^3_0\frac2{15}x^3\ dx + \int\limits^5_3\frac15(5x^2-x^3)\ dx-\frac{64}{9}$$
> $$\text{Var}(X)=\frac{2}{15}\int\limits^3_0x^3\ dx + \frac15\int\limits^5_3(5x^2-x^3)\ dx-\frac{64}{9}$$
> $$=\frac{1}{30}\left[x^4\right]^3_0+\frac15\left[\frac53x^3-\frac14x^4\right]^5_3-\frac{64}{9}$$
> $$=\frac{27}{10}+\frac{82}{15}-\frac{64}{9}$$
> $$=\frac{19}{18}$$

## Centiles
The **median**, $Q_2$, is the cumulative distribution function such that $F(m)=0.5$.

The **lower quartile**, $Q_1$, is the cumulative distribution function such that $F(m)=0.25$.

The **upper quartile**, $Q_3$ is the cumulative distribution function such that $F(m)=0.75$.

## Mode
The **mode** is such that $f(x)$ is a maximum. This will either occur at a turning point or a boundary.
$$f(a), f(b), \frac{df}{dx}=0$$ are the three locations that need to be checked. The greatest of those will be the mode.

> [!Example]
> A random variabvle $X$ has the following PDF:
> $$f(x)=\left\{
> \begin{matrix}
> \frac3{80}(8+2x-x^2),&0\leq x \leq 4 \\
> 0 & \text{otherwise}
> \end{matrix}\right\}
> $$
> Determine the CDF and the mode of $X$.
> \
> $$\frac3{80}\int\limits^x_0(8+2t-t^2)\ dt=\frac3{80}\left[8t+t^2-\frac13t^3\right]^x_0=\frac{3}{80}(8x+x^2-\frac13x^3)$$
>
 > $$F(x)=\left\{
> \begin{matrix}
> 0 & x \lt 0 \\
> \frac{3}{80}(8x+x^2-\frac13x^3),&0\leq x \leq 4 \\
> 1 & 4 \lt x
> \end{matrix}\right\}
> $$
>\
> $f(0)=\frac{3}{10}$
>\
> $f(4)=0$
>\
> $$f'(x)=0 \rightarrow -\frac3{40}x+\frac3{40}=0 \rightarrow (x=1)$$
> $$f(1)=\frac{27}{80}$$
> Mode is $x=1$.

> [!Example]
> A random variable $X$ has the following CDF
> $$F(x)= \left\{ 
> \begin{matrix}
> 0 & x \lt 1 \\
> \frac15x - \frac15 & 1 \leq x \leq 2 \\
> \frac1{10}x^2 - \frac15x + \frac15 & 2 \lt x \lt 4 \\
> 1 & 4 \leq x
> \end{matrix} \right\}
> $$
> Find the interquartile range
> \
> $$Q_3-Q_1=F^{-1}(0.75)-F^{-1}(0.25)$$
> $$0.1x^2-0.2x+0.2=0.25$$
> $$x^2-2x+2=2.5$$
> $$x^2-2x-0.5=0$$
> $$x=Q_1=\frac{2+\sqrt{6}}{2}$$
> $$0.1x^2-0.2x+0.2=0.75$$
> $$x^2-2x-5.5=0$$
> $$Q_3=\frac{2+\sqrt{26}}{2}$$
> $$Q_3-Q_1\approx 1.32$$

# Functions of Random Variables
Assume $X$ is a random variable and $Y=g(X)$, then $Y$ itself is a random variable.

First note that the range of $Y$ can be written as:
$$R_Y=\{g(x)|x\in R_X\}$$

## Finding the PDF
Given the PDF of $X$, $f(x)$, such that

$$f(x)=\left\{\begin{matrix}
f_0(x) & a \lt x \lt b \\
f_1(x) & b \leq x \leq c \\
0 & \text{otherwise}
\end{matrix}\right\}$$

we now investigate the PDF of $Y$, $h(y)$:

$$Y=g(X)$$
$$X=g^{-1}(Y)$$
$$f(X) \rightarrow f_0(g^{-1}(Y))$$
$$f_1(g^{-1}(Y))$$
$$\downarrow$$
$$h(y)=\left\{\begin{matrix}
f_0(g^{-1}(y)) & g(a) \lt y \lt g(b) \\
f_1(g^{-1}(y)) & g(b) \leq x \leq g(c) \\
0 & \text{otherwise}
\end{matrix}\right\}$$

> [!Danger]
> This relies on $g$ being an increasing function.

$$P_Y(y) = P(Y=y)$$
$$=P(g(X)=y)$$

The PDF of the random variable $Y$, at a value of $y$, is equal to the probability of the random variable $Y$ having the value of $y$.

Because, we know that $Y$ is equal to $g(X)$, we can say the the PDF of $Y$ is equal to $P(g(X)=y)$.

What this probability function is asking is: "when is $g(X)=y$?". This can occur on multiple occasions. Therefore, our probability be the sum total total of all of the outputs of $g(X)$ such that $g(X)=y$. Therefore, 

$$=\sum_{x:g(x)=y}P_X(x)$$
$$X = g^{-1}(Y)$$
$$=\sum_{y:
g(x)=y}P_X(g^{-1}(y))$$

## Finding the CDF
Given the CDF of $X$, $F(x)$, we find the CDF of $Y$ of $g(x)$
$$H_Y(y)=P(Y\leq y)$$
$$=P(g(X) \leq y)$$
$$=P(X\leq g^{-1}(y))$$
$$=F(g^{-1}(y))$$
$$\downarrow$$
$$H_Y(\alpha)=F_X(g^{-1}(\alpha))$$

> [!Danger]
> $g$ must be an increasing function!

> [!shortcut]
> $$\text{CDF}=\int\limits^x_{-\infty}\text{PDF}\ dx$$
> thus,
> $$H_Y(y)=\int\limits^{g^{-1}(y)}_{-\infty}f(t)\ dt$$
> The inverse can be done as well (differentiating the CDF of $Y$ to obtain the PDF of $X$)

|              | $X$                                    |                                                                        | $Y=g(x)$                                |
| ------------ | -------------------------------------- | ---------------------------------------------------------------------- | --------------------------------------- |
| $\text{PDF}$ | $f(x)$                                 | $💀\rightarrow$                                                        | $h(y)=\frac{d}{dy}\left[F(g(y))\right]$ |
|              | $$\downarrow \text{integrate}$$        | $\searrow \text{integrate with}\ g^{-1}(y)\ \text{as the upper bound}$ | $\uparrow \text{differentiate}$         |
| $\text{CDF}$ | $\int\limits^x_{-\infty}f(t)\ dt=F(x)$ | $\rightarrow [y=g(x) \implies x=g^{-1}(y)]$                            | $H(y)=F(g^{-1}(y))$                     |

> [!example]
> $X$ is a continuous random variable such that $X$ is distributed uniformly between $0$ and $1$ ($X \sim U(0,1)$.
>
> Find the PDF of $Y$ such that $Y=e^X$
>
> $$f_X(x)=\left\{\begin{matrix}
> 1 & 0 \leq x \leq 1 \\
> 0 & \text{otherwise}
> \end{matrix}\right\}$$
> Integrate to find the CDF
> $$F_X(x)=\left\{\begin{matrix}
> 0 & x \lt 0 \\
> x & 0 \leq x \leq 1 \\
> 1 & 1 \lt x
> \end{matrix}\right\}$$
>
> $$X=\ln Y \implies x=\ln y$$
>
> $$F_X(\ln y)=\left\{\begin{matrix}
> 0 & \ln y \lt 0 \\
> \ln y & 0 \leq \ln y \leq 1 \\
> 1 & 1 \lt \ln y
> \end{matrix}\right\}$$
>
> Because, $e^x$ is an increasing function, the boundaries can be updated
>
> $$F_Y(y)=\left\{\begin{matrix}
> 0 & e^{\ln y} \lt e^0 \\
> \ln y & e^0 \leq e^{\ln y} \leq e^1 \\
> 1 & e^1 \lt e^{\ln y}
> \end{matrix}\right\}$$
>
> $$F_Y(y)=\left\{\begin{matrix}
> 0 & y \lt 1 \\
> \ln y & 1 \leq y \leq e \\
> 1 & e \lt y
> \end{matrix}\right\}$$
> Differentiate to find the PDF.
> $$\downarrow$$
> $$f_Y(y)=\left\{\begin{matrix}
> \frac1y & y \in [1,e] \\
> 0 & y \notin [1,e]
> \end{matrix}\right\}$$


> [!Example]
> Let $X$ be a continuous random variable with PDF given by 
> $$p(x)=\frac12e^{-|x|},\quad \forall x \in \mathbb{R}$$
> If $Y=X^2$, find the CDF of $Y$.
> 
> ![[Continuous Random Variables 2023-02-15 10.37.09.excalidraw]]
> 
> $$p(x)=\left\{\begin{matrix}
> \frac12e^x & 0 \geq x \\
> \frac12e^{-x} & 0 \lt x
> \end{matrix}\right\}$$
> \
> $$\frac12\int\limits^x_{-\infty}e^t\ dt=\frac12\left[e^t\right]^x_{-\infty}=\frac12[e^x-e^{-\infty}]$$
> $$\lim\limits_{k\to\infty}\left[\frac12e^x-\frac12e^{-k}\right]=\frac12e^x-0=\frac12e^x$$
> \
> $$\frac12\int\limits^x_{0}e^{-t}\ dt=\frac12\left[-e^{-t}\right]^x_{0}=-\frac12[e^{-x}-e^{-0}]=-\frac12e^{-x}+\frac12$$
> 
> $$P(x)=\left\{\begin{matrix}
> \frac12e^x & 0 \geq x \\
> -\frac12e^{-x}+\frac12 & 0 \lt x
> \end{matrix}\right\}$$
>
> $$Y=X^2 \implies X=\sqrt{Y}$$
>
> $$P(\sqrt{y})=\left\{\begin{matrix}
> \frac12e^\sqrt{y} & 0 \geq \sqrt{y} \\
> -\frac12e^{-\sqrt{y}}+\frac12 & 0 \lt \sqrt{y}
> \end{matrix}\right\}$$
> > [!warning]
> > $$0 \geq \sqrt{y}\ \text{is undefined.}$$
> > A different method must be used.
>
>  From definitions:
> $$F_Y(y)=P(Y\leq y)$$
> by substituting $X^2$ into $Y$,
> $$P(Y \leq y) = P(X^2 \leq y)$$
> by rearranging the inequality we find an upper and lower bound of $x$, okay
> $$P(X^2 \leq y) = P(-\sqrt{y} \leq X \leq \sqrt{y})$$
> by definition of probability between two values as integration of the PDF,
> $$P(-\sqrt{y} \leq X \leq \sqrt{y})=\int\limits^\sqrt{y}_{-\sqrt{y}}\frac12 e^{-|x|}\ dx$$
> by symmetry, the following integral can be evaluated
> $$\int\limits^\sqrt{y}_{-\sqrt{y}}\frac12 e^{-|x|}\ dx=2\int\limits^\sqrt{y}_0\frac12e^{-x}\ dx=\int\limits^\sqrt{y}_0e^{-x}\ dx$$
> $$-\left[e^{-x}\right]^\sqrt{y}_0=-e^{-\sqrt{y}}+1$$
> Thus, 
> $$F_Y(y)=\left\{\begin{matrix}
> 0 & y \lt 0 \\
> -e^{-\sqrt{y}} + 1 & y \geq 0
> \end{matrix}\right\}$$

##  Expected Values of Functions of Random Variables
$$\text{let}\ E_A(b)=\int b \times f_A(t)\ dt$$
Where:
- $A$ is a CRV with PDF $f_A(t)$
- $b$ is a function of $t$

\
\
\
Suppose we are given a CRV $X\sim f_X(x)$.

We can find $E_X(X)=\int x\times f_X(x)\ dx$

Thus, it stands to reason that, for $Y=g(X)$ with a PDF $f_Y(y)$,
$$E_Y(Y)=\int y \times f_Y(y)\ dy$$
A shortcut can be taken here, without needing to calculate the PDF of $Y$:
$$\mu_Y=E_X(Y)=E_X\left(g\small{(x)}\right)=\int g(x) \times f_X(x)\ dx$$
Similarly...
$$\text{Var}_X(X)=E_X(X^2)-E_X(X)^2$$
$$\text{Var}_Y(Y)=E_Y(Y^2)-E_Y(Y)^2$$
$$\downarrow$$
$$\text{Var}_X(Y)=\text{Var}_X(g(X))=E_X(g(X)^2)-E_X(g(X))^2$$
$$=E_X(g(X)^2)-\mu_{Y}^2$$
$$=\int g(x)^2 \times f_X(x)\ dx - \mu_Y^2$$
