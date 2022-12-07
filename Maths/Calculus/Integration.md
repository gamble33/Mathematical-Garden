# By Substitution
## Boring Version
The goal of the boring version is to simplify a complex-looking expression.

Find an expression, $g(x)$, in the integrand, $\int\limits^a_b{f(g(x))\space dx}$, which is complex-looking. 

Say $u=g(x)$.

Find the new limits $a\prime=g(a)$ and $b\prime=g(b)$.

rearrange 
$$u=g(x) \to x=g^{-1}(u)$$
differentiate with respect to $u$.
$$\frac{dx}{du}=[g^{-1}(u)]'$$
$$dx=du[g^{-1}(u)]'$$

Rewrite the new integral as
$$\int\limits^{a\prime}_{b\prime}{f(u)\times[g^{-1}(u)]' \space du}$$

## *Extreme* Version
The goal of the extreme version is to complexify a simple-looking expression.

Write an expression, $g(u)$ and place it in the integrand, $\int\limits^a_b{f(x)\space dx}$, which is simple-looking. 

Say $x=g(u)$.

Find the new limits $a\prime=g^{-1}(a)$ and $b\prime=g^{-1}(b)$.

differentiate with respect to $u$.
$$\frac{dx}{du}=g'(u)$$
$$dx=du\times g'(u)$$

Rewrite the new integral as
$$\int\limits^{a\prime}_{b\prime}{f(g(u))\times g'(u) \space du}$$

> [!Example]
> $$\int{\frac{1}{1+x^2}dx}=\arctan{x}+C$$
> $$x=\tan{\theta} \to \theta = \arctan{x}$$
> $$\frac{dx}{d\theta} = sec^2{\theta} \to dx=\sec^2{\theta} \space d\theta$$
> $$\implies \therefore \to \int\frac{1}{1+\tan^2{\theta}}\times\sec^2{\theta}\space d\theta$$
> > [!Lalala] 
> > remember: $\tan^2{\theta}+1\equiv\sec^2{\theta}$
>
> $$=\int{\frac{1}{\sec^2{\theta}} \times \sec^2{\theta}\space d\theta}$$
> $$=\int{1 \space d\theta}$$
> $$=\theta=\arctan{x}$$

> [!Example]
> $$\int{\frac 1 {\sqrt{a^2 + x^2}} \space dx}$$
> $$x=a\times\tan{\theta}$$
> $$\frac{dx}{d\theta}=a\times\sec^2\theta\to dx=a\times\sec^2\theta\times d\theta$$
> $$\int{\frac 1 {\sqrt{a^2 + a^2\times\tan^2{\theta}}} \space dx}$$
> $$\int{\frac 1 {\sqrt{a^2(1+\tan^2{\theta})}} \space dx}$$
> $$\int{\frac 1 {a\sqrt{(1+\tan^2{\theta})}} \space dx}$$
> $$\int{\frac 1 {a\sqrt{(\sec^2{\theta})}} \space dx}$$
> $$\int{\frac 1 {a\sqrt{(\sec^2{\theta})}} \times a\times sec^2\theta \space d\theta}$$
> $$\int{\frac 1 {\sec{\theta}} \times sec^2\theta \space d\theta}$$
> $$\int{\frac{1}{\cos\theta}\space d\theta}$$
> $$=\ln{|\sec{\theta}+\tan{\theta}|}+C$$
> $$=\ln{\left|\sqrt{1+\frac{x^2}{a^2}}+\frac{x}{a}\right|}$$
> $$=\text{arsinh}\space{x}+C$$

> [!Example]
> $$\int{\frac{1}{\sqrt{x^2-a^2}}\space dx}$$
> x = sinh($\theta^2%$)

# Integrating Reciprocal Quadratics
## (by partial fractions)
It is appropriate to use a partial fraction integration method when the polynomial, $p_n(x)$, in the integral, $\int{\frac{1}{p_n(x)}}dx$, can be factorised into real linear terms.
> [!Example]
> $$\int{\frac 1 {x^2 + 3x - 4}}dx$$
> $$=\int{\frac 1 {(x+4)(x-1)}}dx$$
> $$\frac 1 {(x+4)(x-1)}=\frac A {x+4} + \frac B {x-1}$$
> $$1=A(x-1) + B(x+4)$$
> substitute $x=1$,
> $$1 = 5B \to B=\frac 1 5$$
> substitute $x=-4$,
> $$1=-5A \to A = -\frac 1  5$$
> $$=\int{\frac 1 {5(x-1)} - \frac 1 {5(x+4)} }dx$$
> $$=\frac 1 5 \int{\frac 1 {(x-1)} - \frac 1 {(x+4)} }dx$$
> $$=\frac 1 5 \left[\ln{(x-1)} - \ln{(x+4)}\right]$$
> $$=\frac 1 5 \ln{\frac{x-1}{x+4}}$$

## (by completing the square)
It is appropriate to integrate by completing the square if the polynomial is in a square root. Or, if it has no real roots. Or if you don't want to use the partial fraction method because completing the square will work either way.
> [!Example]
> Determine $\int \frac 1 {x^2 - 8x + 36} \space dx$
> 
> complete the square
> $$=\int \frac 1 {(x-4)^2 + 20} \space dx$$
> $$=\int \frac 1 {(x-4)^2 + \sqrt{20}^2} \space dx$$
> use the substitution $u=x-4$
> $$x=u+4$$
> $$\frac {dx} {du} = 1$$
> $$dx=du$$
> $$=\int \frac 1 {u^2 + \sqrt{20}^2} \space du$$
> by standard result
> $$= \frac {1} {\sqrt{20}} \arctan{\left(\frac u {\sqrt{20}}\right)}$$
> $$= \frac {1} {\sqrt{20}} \arctan{\left(\frac {x-4} {\sqrt{20}}\right)}$$

> [!Example]
> Determine $\int \frac 1 {\sqrt{2x^2 + 12x}}\space dx$
>
> take a factor of $\frac {1} {\sqrt{2}}$ out,
> $$\frac{1}{\sqrt{2}} \int \frac 1 {\sqrt{x^2 + 6x}}\space dx$$
> $$=\frac 1 {\sqrt{2}} \int \frac 1 {\sqrt{(x+3)^2-3^2}}\space dx$$
> $$=\frac 1 {\sqrt{2}} \int \frac 1 {\sqrt{(x+3)^2-3^2}}\space dx$$
> substitute $u = x + 3$
> $$x=u-3$$
> $$dx=du$$
> $$=\frac 1 {\sqrt{2}} \int \frac 1 {\sqrt{u^2-3^2}}\space du$$
> by standard result:
> $$=\frac 1 {\sqrt 2}\text{arcosh}\space{\left(\frac {u} {3}\right)} + C$$
> $$=\frac 1 {\sqrt 2}\text{arcosh}\space{\left(\frac {x+3} {3}\right)} + C$$

> [!Warning]
> These are all standard results that may not be instantly noticeable.
> $$\int { \sqrt{ \frac {1} {x^2 - 9} }  } \space {dx} \equiv \int { \frac {1} {\sqrt{x^2 - 3^2}} } \space {dx}$$
> $$\int { \left(x^2-9\right)^{-\frac 1 2} \space dx} \space {dx} \equiv \int { \frac {1} {\sqrt{x^2 - 3^2}} } \space {dx}$$
> $$\int {\frac {1} {(x+3)(x-3)}} \space {dx} \equiv \int { \frac {1} {x^2-3^2} } \space {dx}$$

# Integration by Parts
$$\int (f(x)\times g(x)) dx \equiv f(x)\times G(x) - \int {f'(x)\times G(x)\space dx}$$
## Unit Method
We pick 
$$g(x)=1$$
$$f(x)=\text{target integrand}$$
Hope: make integral easier to solve.

> [!Example]
> $$\int \ln{x} \space dx$$
> $$\begin{matrix}f(x)=\ln{x}&f'(x)=\frac 1 x \\ g(x)=1 & G(x) = x\end{matrix}$$
> $$=x\ln{x}-\int\frac 1 x\times x \space dx$$
> $$=x\ln{x}-\int 1 \space dx$$
> $$=x\ln{x}-x$$

> [!Example]
> $$\int{\text{artanh}\space x \space dx}$$
> $$\begin{matrix}f(x)=\text{artanh}\space x & f'(x) = \frac{1}{1-x^2}\\ g(x)=1 & G(x)=x\end{matrix}$$
> $$=x\space\text{artanh}\space x - \int \frac x {1 - x^2} \space dx$$
> $$=x\space\text{artanh}\space x - \int \frac x {1 - x^2} \space dx$$
> integrate by observation
> $$=x\space\text{artanh}\space x + \frac 1 2 \ln{\left|1-x^2\right|}+C$$

# Reduction Formulae
> [!Example]
> integrate $\int x^4 e^x \space dx$
>
> consider $I_n = \int x^n e^x \space dx$,
> $$I_n = x^ne^x-n\int x^{n-1}e^x \space dx$$
> $$I_n = x^ne^x-nI_{n-1}$$
> $$I_0=e^x$$
> $$I_1=e^x(x-1)$$
> $$I_2=x^2e^x-2e^x(x-1)=e^x(x^2-2x+2)$$
> $$I_3=x^3e^x-3[e^x(x^2-2x+2)]=e^x(x^3-3x^2+6x-6)$$
> $$I_4=x^4e^x-4[e^x(x^3-3x^2+6x-6)]$$
> $$I_4=e^x(x^4-4x^3+12x^2-24x+24)$$
> $$I_n=e^x\sum\limits^n_{r=0}(-1)^r\frac{n!}{r!}x^r$$

>[!Example]
> $$I_n=\int\limits^0_1 x^n (1-x)^\frac{1}{2}\space dx$$
> $$= \left[x^n\left(-\frac 2 3\right)(1-x)^{\frac{3}{2}}\right]^0_1-\int\limits^0_1 nx^{n-1} \left(-\frac 2 3\right)(1-x)^{\frac{3}{2}}\space dx$$
> $$= n \left(\frac 2 3\right) \int\limits^0_1 x^{n-1} (1-x)^{\frac{3}{2}}\space dx$$
> $$= n \left(\frac 2 3\right) \int\limits^0_1 x^{n-1} (1-x)(1-x)^{\frac{1}{2}}\space dx$$
> $$= n \left(\frac 2 3\right) \int\limits^0_1 (x^{n-1}-x^n)(1-x)^{\frac{1}{2}}\space dx$$
> $$= n \left(\frac 2 3\right) \left[ \int\limits^0_1 x^{n-1}(1-x)^{\frac{1}{2}}\space dx-\int\limits^0_1x^n(1-x)^{\frac{1}{2}}\space dx \right]$$
> $$= n \left(\frac 2 3\right) (I_{n-1}-I_n)=I_n$$
> $$\left(\frac 2 3 n + 1\right)I_n=n \left(\frac 2 3\right) I_{n-1}$$
> $$I_n=\frac{n \left(\frac 2 3\right) I_{n-1}}{\left(\frac 2 3 n + 1\right)}$$
> $$I_n=\frac{2n I_{n-1}}{2n + 3}$$

> [!Example]
> Integrate $\int^{\frac \pi 2}_0\sin^n{x}\ dx,\ n\geq 0$
> $$I_n=\int^{\frac \pi 2}_0\sin^n{x}\ dx$$
> $$\begin{matrix}f(x)=\sin^{n-1}{x}&f'(x)=(n-1)(\cos{x})(\sin^{n-2}{x})\\ g(x)=\sin{x}&G(x)=-\cos{x}\end{matrix}$$
> $$I_n=-\left[(\cos{x})(\sin^{n-1}{x})\right]^{\frac \pi 2}_0 + (n-1)\int^{\frac \pi 2}_0 (\cos^2{x})(\sin^{n-2}{x})dx$$
> $$=(n-1)\int^{\frac \pi 2}_0 (1-\sin^2{x})(\sin^{n-2}{x})dx$$
> $$=(n-1)\left[\int^{\frac \pi 2}_0 \sin^{n-2}dx-\int^{\frac \pi 2}_0 \sin^{n}dx\right]$$
> $$=(n-1)\left[I_{n-2}-I_n\right]=I_n$$
> $$I_n=\frac{I_{n-2}(n-1)}{n}$$