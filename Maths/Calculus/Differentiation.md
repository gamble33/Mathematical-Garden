# Definitions
## Power Series
$$P(x)\equiv\sum\limits^\infty_{i=0}a_ix^i$$
A polynomial with an infinite amount of terms.
## Infinitely Differentiable Function
A function is infinitely differentiable if the function is always differentiable at a point.

> [!Note]
> If a function is infinitely differentiable, it is smooth.

> [!Example]
> Examples of smooth functions
> $$\sin{x}$$
> $$p_n(x)\space\text{(polynomials)}$$
> $$e^x$$

> [!Example]
> Examples of non-smooth functions
> $$\frac1x\text{ at the point }x=0$$

# Implicit Differentiation
- Differentiate each side of the equation (using chain rule if necessary).
- Remember that $y$ differentiated with respect to $x$ is, by definition, $\frac {dy} {dx}$.



> [!Tip]
> When finding an implicit second derivative. Don't start by differentiating the first implicit derivative. Rather, start with the original implicit equation and apply two derivatives to each term.
> > [!Example]
> > Find the exact value of the second derivative at the point $(0, 0)$.
> > $$x^2=ye^x+y^2$$
> > apply the first derivative:
> > $$2x=e^xy+y'e^x+2yy'$$
> > apply the second derivative:
> > $$2=e^xy+y'e^x+y''e^x+e^xy'+2\left((y')^2+yy''\right)$$
> > $$2=e^xy+2y'e^x+y''e^x+2y'^2+2yy''$$
> > $$2-e^xy-2\frac{dy}{dx}e^x-2\left(\frac{dy}{dx}\right)^2=\frac{d^2y}{dx^2}\times(e^x+2y)$$
> > $$\frac{2-e^xy-2\frac{dy}{dx}e^x-2\left(\frac{dy}{dx}\right)^2}{e^x+2y}=\frac{d^2y}{dx^2}$$
> > rearrange  to make the first derivative the subject:
> > $$\frac{dy}{dx}=\frac{2x-e^xy}{e^x+2y}$$
> > $$\frac{dy}{dx}|_{(0,0)}=\frac{0}{1}=0$$
> > evaluate the second derivative:
> > $$\vdots$$
> > $$\frac{d^2y}{dx^2}|_{(0,0)}=2$$

> [!Tip]
> If you're evaluating a derivative at a point. Don't rearrange the equation, rather substitute in the given values to avoid heavy lifting.
> > [!Example]
> > Find the exact value of the second derivative at the point $(0, 0)$.
> > $$x^2=ye^x+y^2$$
> > apply the first derivative:
> > $$2x=e^xy+y'e^x+2yy'$$
> > substitute the coordinate $(0,0)$ to find the first derivative evaluated at this point:
> > $$0=0+y'+0\implies\frac{dy}{dx}=0$$
> > 
> > apply the second derivative:
> > $$2=e^xy+y'e^x+y''e^x+e^xy'+2\left((y')^2+yy''\right)$$
> > 
> > substitute the coordinate $(0,0)$:
> > $$2=0+y'+y''+y'+2(y')^2$$
> > substitute in $\frac{dy}{dx}|_{(0,0)}=y'|_{(0,0)}=0$
> > $$2=0+0+y''+0+0$$
> > $$\frac{d^2y}{dx^2}|_{(0,0)}=2$$

# Parametric Differentiation
If $x$ and $y$ are both given in terms of the parameter $t$ where $x=f(t)$ and $y=g(t)$, then the gradient function $\frac{dy}{dx}$ is given by the quotient $\frac{g'(t)}{f'(t)}$.

This is due to the chain rule.
$$\frac{dy}{dx}\equiv\frac{dy}{dt}\times\frac{dt}{dx}$$

> [!Warning]
> This will yield the gradient function in terms of the parameter $t$.

## Second Derivative
In order to find the second derivative of $y$ with respect to $x$. We would need to differentiate the first derivative of $y$ with respect to $x$. However, that first derivative will be written in terms of $t$. Therefore, we would need to apply the chain rule a second time.

$$y=g(t),\space x=f(t)$$
$$\frac{dy}{dt}=g'(t),\space\frac{dx}{dt}=f'(t)$$
$$\frac{dy}{dx}=\frac{\frac{dy}{dt}}{\frac{dx}{dt}}=\frac{g'(t)}{f'(t)}=h(t) \space \text{(the gradient function, A.K.A. the first derivative)}$$
$$\frac{d^2y}{dx^2}=\frac{d\left(h(t)\right)}{dx}=\frac{d\left(h(t)\right)}{dt}\times\frac{dt}{dx}$$
$$=\frac{h'(t)}{f'(t)}$$

# Hyperbolic Differentiation
## First Principles $\frac{d\sinh{x}}{dx}$
$$\frac{d\sinh{x}}{dx}=\lim_{\delta\to0}\left[\frac{\sinh{(x+\delta)}-\sinh{(x)}}{\delta}\right]$$
$$=\lim_{\delta\to0}\left[\frac{e^xe^\delta-e^{-x}e^{-\delta}-e^x+e^{-x}}{2\delta}\right]$$
$$=\lim_{\delta\to0}\left[\frac{e^xe^\delta-e^{-x}e^{-\delta}-e^x+e^{-x}}{2\delta}\right]$$
$$=\lim_{\delta\to0}\left[\frac{e^x(e^\delta-1)-e^{-x}(e^{-\delta}-1)}{2\delta}\right]$$
$$=\frac{1}{2}\lim_{\delta\to0}\left[\frac{e^x(e^\delta-1)-e^{-x}(e^{-\delta}-1)}{\delta}\right]$$
$$=\frac{1}{2}\lim_{\delta\to0}\left[\frac{e^x(e^\delta-1)}{\delta}\right]-\frac{1}{2}\lim_{\delta\to0}\left[\frac{e^{-x}(e^{-\delta}-1)}{\delta}\right]$$
$$=\frac{1}{2}e^{x}\lim_{\delta\to0}\left[\frac{e^\delta-1}{\delta}\right]-\frac{1}{2}e^{-x}\lim_{\delta\to0}\left[\frac{e^{-\delta}-1}{\delta}\right]$$
By the [[Differentiation#Expansion of $e x$]]
$$=\frac{1}{2}e^{x}\lim_{\delta\to0}\left[\frac{(1+\delta+\frac{\delta^2}{2!}+\frac{\delta^3}{3!}+\dots)-1}{\delta}\right]-\frac{1}{2}e^{-x}\lim_{\delta\to0}\left[\frac{(1-\delta+\frac{\delta^2}{2!}-\frac{\delta^3}{3!}+\dots)-1}{\delta}\right]$$
$$=\frac{1}{2}e^{x}\lim_{\delta\to0}\left[1+\frac{\delta}{2!}+\frac{\delta^2}{3!}+\dots\right]-\frac{1}{2}e^{-x}\lim_{\delta\to0}\left[-1+\frac{\delta}{2!}-\frac{\delta^2}{3!}+\dots\right]$$
$$=\frac{1}{2}e^x+\frac{1}{2}e^{-x}$$
$$=\frac{e^x+e^{-x}}{2}$$
$$=\cosh{x}$$

## $\cosh{x}$ derivative
$$\cosh{x}\equiv\frac{e^x+e^{-x}}{2}$$
$$\frac{1}{2}\times\frac{d}{dx}\left(e^x+e^{-x}\right)$$
$$=\frac{1}{2}\left(e^x-e^{-x}\right)$$
$$=\sinh{x}$$

## $\tanh{x}$ derivative
$$[\sinh{x}]'\to\cosh{x}$$
$$[\cosh{x}]'\to\sinh{x}$$
Thus, by quotient rule:
$$\frac{d}{dx}\left(\tanh{x}\right)=\frac{\cosh^2{x}-\sinh^2{x}}{\cosh^2{x}}$$
By [[Hyperbolic Functions#Identities]]
$$=\frac{1}{\cosh^2{x}}$$
$$=\text{sech}^2\space{x}$$

## $\coth{x}$ Derivative
$$[\sinh{x}]'\to\cosh{x}$$
$$[\cosh{x}]'\to\sinh{x}$$
Thus, by quotient rule:
$$\frac{d}{dx}\left(\coth{x}\right)=\frac{\sinh^2{x}-\cosh^2{x}}{\sinh^2{x}}$$
By [[Hyperbolic Functions#Identities]]
$$=\frac{-1}{\sinh^2{x}}$$
$$=-\text{cosech}^2\space{x}$$

## $\text{arsinh}\space{x}$ derivative
Given $y=\text{arsinh}\space{x}$, $\sinh{y}=x$.

By implicit differentiation
$$\cosh{y}\frac{dy}{dx}=1$$
$$\frac{dy}{dx}=\frac{1}{\cosh{y}}=\text{sech}\space{y}$$
$$=\text{sech}\space{(\text{arsinh}\space{x})}$$
$$=\frac{2}{e^{\ln{(x+\sqrt{x^2+1})}}+e^{-(\ln{(x+\sqrt{x^2+1})}}}$$
$$=\frac{2}{(x+\sqrt{x^2+1})+\frac{1}{(x+\sqrt{x^2+1})}}$$
$$=\frac{2(x+\sqrt{x^2+1})}{(x+\sqrt{x^2+1})^2+1}$$
$$=\frac{2(x+\sqrt{x^2+1})}{x^2+2x\sqrt{x^2+1}+x^2+2}$$
$$=\frac{2(x+\sqrt{x^2+1})}{2x^2+2x\sqrt{x^2+1}+2}$$
$$=\frac{x+\sqrt{x^2+1}}{x^2+x\sqrt{x^2+1}+1}$$
Multiply both the numerator and denominator of the fraction by the radical conjugate of $(x+\sqrt{x^2+1})$.
$$=\frac{(x+\sqrt{x^2+1})(x-\sqrt{x^2+1})}{(x^2+x\sqrt{x^2+1}+1)(x-\sqrt{x^2+1})}$$
$$=\frac{x^2-x\sqrt{x^2+1}+x\sqrt{x^2+1}-x^2-1}{(x^2+x\sqrt{x^2+1}+1)(x-\sqrt{x^2+1})}$$
$$=\frac{x^2-x^2-1}{(x^2+x\sqrt{x^2+1}+1)(x-\sqrt{x^2+1})}$$
$$=\frac{-1}{(x^2+x\sqrt{x^2+1}+1)(x-\sqrt{x^2+1})}$$
by expanding and collecting the terms on the denominator:
$$\vdots$$
$$=\frac{-1}{-\sqrt{x^2+1}}$$
$$=\frac{-1}{-\sqrt{x^2+1}}$$
$$=\frac{1}{\sqrt{x^2+1}}$$

## $\text{arcosh}\space{x}$ Derivative
By a similar method to [[Differentiation#$ text{arsinh} space{x}$ derivative|above]]:
$$\frac{d}{dx}\left(\text{arcosh}\space{x}\right)=\frac{1}{\sqrt{x^2-1}}$$

## $\text{artanh}\space{x}$ Derivative
By a similar method to [[Differentiation#$ text{arsinh} space{x}$ derivative|above]]:
$$\frac{d}{dx}\left(\text{artanh}\space{x}\right)=\frac{1}{1-x^2}$$


# MacLaurin Explansion
Any [[Differentiation#Infinitely Differentiable Function|smooth function]] can be expressed as a [[Differentiation#Power Series|power series]].

The $n^\text{th}$ derivative of the smooth function will match the $n^\text{th}$ derivative of the power series at the point $x=0$.

## Derivation
Let $f(x)$ be a smooth function.
$$f(x)=a_0x^0+a_1x^1+a_2x^2+a_3x^3+a_4x^4+a_5x^5+\dots$$
$$f(0)=0!\times a_0$$
---
$$f'(x)=0+a_1+2a_2x^1+3a_3x^2+4a_4x^3+5a_5x^4+\dots$$
$$f'(0)=1!\times a_1$$
---
$$f''(x)=0+0+2a_2+(3\times2)a_3x^1+(4\times3)a_4x^2+(5\times4)a_5x^3+\dots$$
$$f''(0)=2!\times a_2$$
---
$$f'''(x)=0+0+0+(3\times2\times1)a_3+(4\times3\times2)a_4x^1+(5\times4\times3)a_5x^2+\dots$$
$$f'''(0)=3!\times a_3$$
$$\vdots$$
$$f^n(0)=n!\times a_n$$
Thus, $f(x)$ must be equal to $\frac{f(0)}{0!}+\frac{f'(0)}{1!}x+\frac{f''(0)}{2!}x^2+\dots+\frac{f^n(0)}{n!}x^n+\dots$
## Ta$y$lor Series
A more general case of the MacLaurin series, centred at any value. Useful for integration around a specific part of the curve for a function that has a limited radius of convergence.


Thus, $f(x)$ must be equal to $\frac{f(a)}{0!}+\frac{f'(a)}{1!}(x-a)+\frac{f''(a)}{2!}(x-a)^2+\dots+\frac{f^n(a)}{n!}(x-a)^n+\dots$

## Expansion of $\sin(x)$
$$a_0 = \sin{0}=0$$
$$a_1=\cos{0}=1$$
$$a_2=\frac{-\sin{0}}{2}=0$$
$$a_3=\frac{-\cos{0}}{6}=-\frac{1}{6}$$
$$a_4=\frac{\sin{0}}{24}=0$$
$$\vdots$$
$$\sin{x}=\frac{1}{1!}x-\frac{1}{3!}x^3+\frac{1}{5!}x^5-\frac{1}{7!}x^7+\dots+(-1)^{n}\frac{1}{(2n+1)!}x^{(2n+1)}+\dots$$
![[Pasted image 20221130120408.png]]

> [!Note
> We can see that the curve matches up pretty much exactly around $x=0$. However, even at other values of $x$, we can see the curve is starting to match. If the expansion eventually matches up for all values of $x$, it is known as an **`entire function`**. Exponential functions and other trigonometric functions are also **`entire`**.

## Expansion of $\cos{(x)}$
$$\cos{x}=\frac{1}{1!}-\frac{1}{2!}x^2+\frac{1}{4!}x^4-\frac{1}{6!}x^6+\dots+(-1)^{n}\frac{1}{(2n)!}x^{(2n)}+\dots$$

## Expansion of $e^x$
$$e^x=\text{exp}(x)=1+x+\frac{x^2}{2!}+\dots\frac{x^r}{r!}+\dots$$

## Expansion of $\ln{(1+x)}$
$$f(x)=\ln{(1+x)}$$
$$f'(x)=(1+x)^{-1}$$
$$f^n(x)=(-1)^n\times(n-1)!\times(1+x)^{-n}$$
$$f(0)=0=a_0$$
$$f'(0)=1=a_1$$
$$f''(0)=-1=(2!)a_2 \to a_2=-\frac 1 2$$
$$f'''(0)=2=(3!)a_3\to a_3=\frac 1 3$$

$$\ln{(1+x)}=x-\frac 1 2 x^2 + \frac 1 3 x^3 + \dots+(-1)^n\frac{1}{n}x^n+\dots,\space n\neq0$$

> [!Example]
> $$\ln{(1+x)}\approx x-\frac 1 2 x^2 + \frac 1 3 x^3 $$
> $$\ln{(1.05)}=\ln{(1+0.05)}\approx 0.04879$$
> $$\ln{(1.25)}=\ln{(1+0.25)}\approx 0.22$$
> $$\ln{(1.8)}=\ln{(1+0.8)}\approx 1$$

## Compound Expansions
### Expansion of $\cos{x}+\sin{x}$ (summation)
$$\cos{x}+\sin{x}\equiv\frac{2}{1!}+\frac{1}{1!}x-\frac{1}{2!}x^2-\frac{1}{3!}x^3 +\dots+(-1)^n\frac{1}{(2n)!}x^{2n}+(-1)^n\frac{1}{(2n+1)!}x^{2n+1}$$

### Expansion of $\cos {2x^2}$ (composite)
$$\cos{2x^2}\equiv1-\frac{(2x^2)^2}{2!}+\frac{(2x^2)^4}{4!}+\dots$$
$$\equiv1-2x^4+\frac{2}{3}x^8-\frac{4}{45}x^{12}+\dots$$
Plug in (colloquially: `substitute`) $2x^2$ as the argument of the [[Differentiation#Expansion of $ cos{(x)}$|expansion of cos(x)]].

### Expansion of $e^x\cos{x}$ (product)
> [!WARNING]
> Questions will generally ask 

* Expand both factors separately.
* Collate terms.


|                  | $1$              | $x$            | $x^2$          | $\frac{x^3}6$ | $\frac{x^4}{24}$ |
| ---------------- | ---------------- | -------------- | -------------- | ------------- | ---------------- |
| $1$              | $1$              | $x$            | $\frac{x^2}2$  | $\frac{x^3}6$ | $\frac{x^4}{24}$ |
| $-\frac{x^2}2$   | $-\frac{x^2}2$   | $-\frac{x^3}2$ | $-\frac{x^4}4$ |               |                  |
| $\frac{x^4}{24}$ | $\frac{x^4}{24}$ |                |                |               |                  |

$$\equiv 1+x-\frac{x^3}{3}-\frac{x^4}6$$

> [!Example]
> Find the first three non-zero terms of the series expansion of $\ln{\left(\frac{\sqrt{1+2x}}{1-3x}\right)}$, and state the interval in $x$ for which the expansion is valid.
> > [!Hint]
> > Use [[Differentiation#Expansion of $ ln{(1+x)}$|this expansion]].
> 
> $$\ln{\left(\frac{\sqrt{1+2x}}{1-3x}\right)}=\frac{1}{2}\ln{(1+2x)}-\ln{(1-3x)}$$
> $$=\frac{1}{2}\left[2x-2x^2+\frac{8x^3}{3}+\dots\right]-\left[-3x-\frac{9x^2}{2}-9x^3\right]$$
> $$=x-x^2+\frac{4}{3}x^3+3x+\frac92x^2+9x^3$$
> $$=4x+\frac72x^2+\frac{31}3x^3$$
> The radius of convergence of $\ln{(1+x)}$ is such that $|x|\leq 1$.
>
> The convergence of the compound function was dependant on the convergence of its parts.
> $$\text{for }\ln{(1+2x)}: |2x|\leq1 \to |x|\leq\frac12$$
> $$\text{for }\ln{(1-3x)}: |-3x|\leq1 \to |x|\leq\frac13$$
> combining both of these, we have the following:
> $$|x|\leq \frac13$$
