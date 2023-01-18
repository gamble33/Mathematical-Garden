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
The goal of the reduction formula is to create and inductive step that will transform a complicated integral into a integral with a reduced power in the hope that a process of induction can be used to calculate an arbitrarily high power.

$$\int f_n(x)\ dx=g\left(\int f_{n-1}(x)\right)$$
Where:
* $f_n(x)$ is a function of $x$ that contains some constant $n$. (Generally in the power, i.e., $x^n$).

The most common strategy is to integrate by parts which involves differentiating the term involving $n$.

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

# Arc Length
$$S=\int ds $$
Where:
* $ds$ is a small section of the curve.
* $S$ is the arc length.
## $wrt \ dx$
$$=\int \sqrt{1+\left(\frac{dy}{dx}\right)^2}\ dx$$

## $wrt \ dy$
$$S=\int \sqrt{1+\left(\frac{dx}{dy}\right)^2}\ dy$$

## Parametrically ($wrt \ t$)
$$=\int \sqrt{\left(\frac{dx}{dt}\right)^2+\left(\frac{dy}{dx}\right)^2}\ dt$$

## Intuition
$$S=\int ds $$

$$ds =\sqrt{(d x)^2+(d y)^2}$$
![[Pasted image 20221208124814.png]]
$$S=\int \sqrt{(d x)^2+(d y)}$$

our function is likely to be determined by $x$ so we wish to integrate with respect to $x$. Therefore, we will need to find how the arc length changes with respect to $x$ ($\frac{ds}{dx}$), and integrate that term over $x$.

$$S=\int \frac{ds}{dx}\ dx$$
$$=\int \frac {1} {dx} \sqrt{(dx)^2+(dy)^2}\ dx$$
$$=\int \sqrt{\frac{(dx)^2+(dy)^2}{(dx)^2}}\ dx$$
$$=\int \sqrt{\frac{(dx)^2}{(dx)^2}+\frac{(dy)^2}{(dx)^2}}\ dx$$
$$=\int \sqrt{1+\left(\frac{dy}{dx}\right)^2}\ dx$$

However, it may be that we wish to find an arc length with respect to $y$. Therefore, we would need to use $\frac{ds}{dy}$ and integrate over $y$.

$$S=\int \sqrt{1+\left(\frac{dx}{dy}\right)^2}\ dy$$

Alternatively, our function may be defined parametrically and we would need to find an arc length in terms of a parameter $t$.

$$=\int \sqrt{\left(\frac{dx}{dt}\right)^2+\left(\frac{dy}{dx}\right)^2}\ dt$$

> [!Example]
> Find the exact arc length of the arc on the parabola with equation $y= \frac 1 2 x^2$, from the origin to the point $P(4,8)$.
>  $$S^4_0=\int\limits^4_0 \sqrt{1 + \left(\frac{dy}{dx}\right)^2}\ dx$$
>  $$S^4_0=\int\limits^4_0 \sqrt{1 + (x)^2}\ dx$$
> by substitution $x=\sinh{u}$,
>  $$dx=\cosh{u}\times du$$
>  $$u = \text{arsinh}\ x$$
> Thus, the new limits are: $u=\ln{(4+\sqrt{17})}$ and $u=0$,
>  $$S^4_0=\int\limits^{\ln{(4+\sqrt{17})}}_0 \sqrt{1 + \sinh^2 u}\ \cosh u\ du$$
>  $$=\int\limits^{\ln{(4+\sqrt{17})}}_0 \cosh^2 u\ du$$
>  $$=\frac 1 2\int\limits^{\ln{(4+\sqrt{17})}}_0 \cosh 2u+1\ du$$
>  $$=\frac 1 2 \left[\frac12 \sinh{2u}+u\right]^{\ln{4+\sqrt{17}}}_0$$
>  $$\vdots$$
>  $$=\frac{(4+\sqrt{17})^2-\frac{1}{(4+\sqrt{17})^2}}{8}+\frac12\ln{(4+\sqrt{17})}$$
> $$\vdots$$
>  $$S^4_0=\frac 1 2 \ln{(4+\sqrt{17})}+2\sqrt {17}$$

## Fun Fact
> [!Example]
> Find arc length of this circular arc:
> ![[Pasted image 20221208130747.png]]
> we know that this circular arc has the forumla $x^2+y^2=1$
> \
> \
> It can be defined parametrically:
> $$(\sin t, \cos t)$$
> or
> $$y=\cos t$$
> $$x=\sin t$$
> $$\frac {dy} {dt} = - \sin t$$ 
> $$\frac {dx} {dt} = \cos t$$ 
> the limits are ($t=0$ and $t=\frac \pi 2$)
> $$S=\int\limits^{\frac \pi 2}_0 \sqrt{\left(\frac{dx}{dt}\right)^2+\left(\frac{dy}{dx}\right)^2}\ dt$$
> $$=\int\limits^{\frac \pi 2}_0 \sqrt{\left(\cos t\right)^2+\left(-\sin t\right)^2}\ dt$$
> $$=\int\limits^{\frac \pi 2}_0 \sqrt{1}\ dt$$
> $$=\int\limits^{\frac \pi 2}_0 1\ dt$$
> $$=[t]^{\frac \pi 2}_0=\frac \pi 2 - 0$$
> $$= \frac \pi 2$$

> [!Error]
> It is not possible to find the exact length of a general ellipse.
> 
> I wonder why...?

# Surface Area of Revolution

$$A = 2 \pi \int  y \sqrt{1+\left(\frac{dy}{dx}\right)^2} dx$$
## Intuition

$$A = \text {Surface Area of Revolution}$$

![[Pasted image 20221212121843.png]]

The surface area of revolution of a curve can be decomposed into a series of angled bands. These are similar to cylinders but are not cylinders. Each of these angled bands will be the curved surface area of a frustum.

![[Pasted image 20221212122005.png]]

The formula of the surface area of this frustum (highlighted green), $\delta A$,  will be...
$$\delta A = BIG\ CONE - AMALL\ CONE$$
$$\delta A = \pi l_2(y+\delta y) - \pi l_1 y$$
$$l_1 = l_2 - \delta s$$
$$\delta A = \pi l_2(y+\delta y) - \pi (l_2-\delta s) y$$
$$\delta A = \pi \left( l_2y+l_2\delta y - l_2y + y\delta s \right)$$
$$\delta A = \pi \left( l_2\delta y + y\delta s \right)$$

![[Integration 2022-12-12 12.29.04.excalidraw]]

$$\frac {l_2} {l_1} = \frac {y + \delta y} {y}$$
$$\frac {l_2} {l_2-\delta s} = \frac {y + \delta y} {y}$$
multiply both sides by $y(l_2-\delta s)$:
$$yl_2 = (y + \delta y)(l_2-\delta s)$$
$$yl_2 = yl_2 - y \delta s + l_2 \delta y - \delta y \delta s$$
$$0 = - y \delta s + l_2 \delta y - \delta y \delta s$$
$$y \delta s + \delta y \delta s = l_2 \delta y$$
$$l_2=y \frac {\delta s} {\delta y} + \delta s$$

$$\delta A = \pi\left[(y \frac {\delta s} {\delta y} + \delta s)\delta y + y \delta s\right]$$
$$\delta A = \pi\left[y\delta s + \delta y \delta s + y \delta s\right]$$
$$\delta A = \pi\delta s\left[y + \delta y + y \right]$$
$$\delta A = \pi\delta s\left[2y + \delta y \right]$$
$$\frac{\delta A}{\delta x} = \pi\delta s\left[2y + \delta y \right] \times \frac {1} {\delta x}$$
$$\frac{\delta A}{\delta x} = \pi\frac{\delta s}{\delta x}\left[2y + \delta y \right]$$

as $\delta x \to 0$, and $\delta y \to 0$,

$\frac {\delta A} {\delta x} \to \frac {dA}{dx}$ and $\frac {\delta s} {\delta x} \to \frac {ds} {dx}$ 

$$\pi\frac{\delta s}{\delta x}\left[2y + \delta y \right] \to 2 \pi y \frac {ds} {dx}$$

$$A = \int \frac {dA}{dx}dx$$

$$A = \int 2 \pi y \frac {ds} {dx} dx$$

$$\frac{ds}{dx}=\sqrt{1+\left(\frac{dy}{dx}\right)^2}$$

$$A = 2 \pi \int  y \sqrt{1+\left(\frac{dy}{dx}\right)^2} dx$$

## Explicit Function
> [!Example]
> The curve $$y=\frac 13 \sqrt{x}(3-x)$$ is rotated around the $x$-axis. Find the surface area of the surface generated between the $x$-coordinates $1$ and $3$.
> 
> $$\frac {dy}{dx}=\frac12 x^{-\frac12}-\frac12 x^{\frac12}$$
> 
> $$\left(\frac {dy}{dx}\right)^2=\frac14 x^{-1}-\frac12+\frac14x$$
> 
> $$S_x=2\pi\int(\frac13\sqrt{x}(3-x))\sqrt{1+\left(\frac{dy}{dx}\right)^2}dx$$
> $$S_x=\pi\int(\frac13\sqrt{x}(3-x))\sqrt{x^{-1}+x+2}\ dx$$
> $$S_x=\pi\int(\frac13\sqrt{x}(3-x))\sqrt{(x^{\frac12}+x^{-\frac12})^2}\ dx$$
> $$S_x=\pi\int(\frac13\sqrt{x}(3-x))(x^{\frac12}+x^{-\frac12})\ dx$$
> $$\frac13 \pi \left[x^2+3x-\frac13x^3\right]^3_1$$
> $$=\frac13 \pi\left([9+9-9]-[1+3-\frac13]\right)$$
> $$=\frac13 \pi(5+\frac13)$$
> $$=\frac{16}{9}\pi$$
> $$=\frac{16}{9}\pi$$

## Parametric Case
$$x = t - \sin t$$
$$y = 1 - \cos t$$
$$t\in[0,2\pi]$$

$$\frac {dx}{dt} = 1 - \cos t$$
$$\frac {dy}{dt} = \sin t$$

$$S_x=2\pi\int y\sqrt{\left(\frac{dx}{dt}\right)^2+\left(\frac{dy}{dt}\right)^2}\ dt$$
$$\left(\frac{dx}{dt}\right)^2+\left(\frac{dy}{dt}\right)^2=1-2\cos t + \cos^2 t+\sin^2 t$$
$$\left(\frac{dx}{dt}\right)^2+\left(\frac{dy}{dt}\right)^2=2(1-\cos t)$$
$$S_x=\pi2\sqrt{2}\int (1-\cos t)^{\frac32}\ dt$$
$$S_x=\pi2\sqrt{2}\int (1-(1-2\sin^2{\frac12 t}))^{\frac32}\ dt$$
$$S_x=\pi2\sqrt{2}\int (2\sin^2{\frac12 t})^{\frac32}\ dt$$
$$S_x=8\pi\int \sin^3{\frac12 t}\ dt$$
$$S_x=8\pi\int \sin{\frac12 t}(1-\cos^2{\frac t 2})\ dt$$
$$S_x=8\pi\int \sin{\frac12 t}-\sin{\frac12 t}\cos^2{\frac t 2})\ dt$$
$$[S_x]_0^{2\pi}=8\pi\left[-2\cos{\frac t 2}-\frac23cos^3\frac{t}{2}\right]^{2\pi}_0$$
$$=8\pi[2+\frac23+2+\frac23]$$
$$=8\pi[\frac{16}3]$$
$$=\frac{128}{3}\pi$$