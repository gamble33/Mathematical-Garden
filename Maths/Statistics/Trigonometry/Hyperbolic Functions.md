[^1]: Odd and even functions [[Odd and Even Functions]]

# Definition
![[Pasted image 20221107153205.png|400]]
A plot of $x^2-y^2=1$ which can be rewritten as $y=\pm\sqrt{x^2-1}$

$$\text{let}\space A=\text{Area bounded by the x-axis, line-segment and curve}$$
I.e., $A$ is the green area that can be seen in the diagram.
## $$\sinh{x}=\frac{e^x-e^{-x}}{2},x\in\mathbb{R}$$
$$y\left(\frac{A}{2}\right)=\sinh{A}$$

## $$\cosh{x}=\frac{e^{x}+e^{-x}}{2},x\in\mathbb{R}$$
$$x\left(\frac{A}{2}\right)=\cosh{A}$$
## $$\tanh{x}=\frac{\sinh{x}}{\cosh{x}}=\frac{e^x-e^{-x}}{e^x+e^{-x}}$$
$\tanh$ is the gradient of the line segment for a given area.

> [!Note]
> These are the functions found by using these properties of a hyperbolic curve. By using the same definitions for a unit circle. You would get $\sin$, $\cos$, and $\tan$.

$$\text{sech}\space{x}=\frac{1}{\cosh{x}}=\frac{2}{e^x+e^{-x}},x\in\mathbb{R}$$
$$\text{cosech}\space\space{x}=\frac{1}{\sinh{x}}=\frac{2}{e^x-e^{-x}},x\in\mathbb{R},x\neq0$$
$$\coth{x}=\frac{1}{\tanh{x}}=\frac{e^x+e^{-x}}{e^x-e^{-x}},x\in\mathbb{R},x\neq0$$
![[Pasted image 20221107155334.png]]
![[Pasted image 20221107155524.png]]
![[Pasted image 20221107155739.png]]

> [!Note]
> $$\sinh{x}\space\text{and}\space\cosh{x}$$
> have the property that each one is the derivative of the other (similar to $\sin$ and $\cos$).

**Examples**
$$\sinh{3}\approx10$$
$$\tanh{\left(\ln{4}\right)}=\frac{4-\frac14}{4+\frac14}=\frac{16-1}{16+1}=\frac{15}{17}$$
**Hidden Quadratic Example**
$$\sinh{x}=5$$
$$5=\frac{e^x-e^{-x}}{2}$$
$$10=e^x-e^{-x}$$
$$10=e^x-\frac{1}{e^{x}}$$
$$10e^x=\left(e^x\right)^2-1$$
$$\text{let}\space k=e^x$$
$$k^2-10k-1=0$$
$$k=e^{x}=10.0999, e^{x}=-0.099$$

# Inverse
Every hyperbolic function can be inverted, however, the inverses of $\cosh$ and $\text{sech}$ (i.e., $\text{arcosh}$ and $\text{arsech}$) are not a reflection in the line $y=x$ as that would yield not yield a function. 
![[Pasted image 20221108150811.png#invert_B|800]]

|            | $\text{arcosech}$ | $\text{arcoth}$ | $\text{arsech}$ | $\text{artanh}$ |
| ---------- | ----------------- | --------------- | --------------- | --------------- |
| Asymptotes | $y=0,x=0$         | $y=0,x=-1,x=1$  | $x=0$           |  $x=1,x=-1$               |

## Proof
$$\text{arsinh}\space x=\ln\left(x+\sqrt{x^2+1}\right)$$
$$\sinh{x}=\frac{e^{x}-e^{-x}}{2}$$
$$x=\frac{e^{y}-e^{-y}}{2}$$
$$2x=e^{y}-e^{-y}$$
$$2xe^y=e^{2y}-1$$
$$\text{let}\space k=e^y$$
$$2xk=k^2-1$$
$$k^2-2xk-1=0$$
$$k=\frac{2x\pm\sqrt{4(x^2+1)}}{2}$$
$$k=\frac{2x\pm2\sqrt{x^2+1}}{2}$$
$$k=x\pm\sqrt{x^2+1}$$
$$e^y=x\pm\sqrt{x^2+1}$$
$$e^{y}>0\space\text{and}\space\sqrt{x^2+1}>x\implies e^{y}=x+\sqrt{x^2+1}$$ 
$$y=\text{arsinh}\space x=\ln{\left(x+\sqrt{x^2+1}\right)}$$

## Derivation of $\text{arcosh}$
$$\cosh{x}=\frac{e^x+e^{-x}}{2}$$
$$x=\frac{e^y+e^{-y}}{2}$$
$$2x=e^y+e^{-y}$$
$$\text{let}\space k=e^y$$
$$2xk=k^2+1$$
$$k^2-2xk+1=0$$
$$k=\frac{2x\pm2\sqrt{x^2-1}}{2}$$
$$k=x\pm\sqrt{x^2-1}$$
$$e^y=x\pm\sqrt{x^2-1}$$
$$\sqrt{x^{2}-1}<x \space\text{and}\space e^{y}>0 \implies e^y=x\pm\sqrt{x^2-1}$$
However, we want to avoid a one-to-many mapping between $y$ and the RHS.
$$y=\text{arcosh}\space x=\ln{(x+\sqrt{x^{2}-1})},\space x \geq 1$$

$$\text{artanh}\space x=\frac{1}{2}\ln{\frac{1+x}{1-x}},\space|x|<1$$
# Identities
## $$\cosh^2{x}-\sinh^2{x}\equiv1$$
> [!Reminder]
> $$\cos^2{x}+\sin^2{x}\equiv 1$$
### Derivation
$$(\cosh{x}-\sinh{x})(\cosh{x}+\sinh{x})\equiv1$$
$$\left(\frac{e^{x}+e^{-x}}{2}-\frac{e^{x}-e^{-x}}{2}\right)\left(\frac{e^{x}+e^{-x}}{2}+\frac{e^{x}-e^{-x}}{2}\right)\equiv1$$
$$\left(\frac{e^x-e^x+e^{-x}+e^{-x}}{2}\right)\left(\frac{e^x+e^x+e^{-x}-e^{-x}}{2}\right)\equiv1$$
$$\left(\frac{2e^{-x}}{2}\right)\left(\frac{2e^x}{2}\right)\equiv1$$
$$\left(e^{-x}\right)\left(e^x\right)\equiv1$$
$$e^{-x+x}\equiv1$$
$$e^{0}\equiv1$$

## $$1-\tanh^{2}{x}\equiv \text{sech}^{2}\space{x}$$
> [!Reminder]
> $$1+\tan^2{x}=\sec^2{x}$$
### Proof
$$(1+\tanh{x})(1-\tanh{x})\equiv\text{sech}^{2}{x}$$
$$\left(1+\frac{e^x-e^{-x}}{e^x+e^{-x}}\right)\left(1-\frac{e^x-e^{-x}}{e^x+e^{-x}}\right)\equiv\text{sech}^{2}{x}$$
$$\left(\frac{e^x+e^{-x}}{e^x+e^{-x}}+\frac{e^x-e^{-x}}{e^x+e^{-x}}\right)\left(\frac{e^x+e^{-x}}{e^x+e^{-x}}-\frac{e^x-e^{-x}}{e^x+e^{-x}}\right)\equiv\text{sech}^{2}{x}$$
$$\left(\frac{2e^x}{e^x+e^{-x}}\right)\left(\frac{2e^{-x}}{e^x+e^{-x}}\right)\equiv\text{sech}^{2}{x}$$
$$\frac{4}{(e^x+e^{-x})^2}\equiv\text{sech}^{2}{x}$$
$$\frac{2^2}{\left(e^x+e^{-x}\right)^2}\equiv\text{sech}^{2}{x}$$
$$\left(\frac{2}{e^x+e^{-x}}\right)^2\equiv\text{sech}^{2}{x}$$

## $$\coth^{2}{x}-1\equiv\text{cosech}^{2}{x}$$
> [!Reminder]
> $$\cot^2{x}+1\equiv\csc^2{x}$$
## Proof
$$\left(\coth{x}-1\right)\left(\coth{x}+1\right)\equiv\text{cosech}^{2}{x}$$
$$\left(\frac{e^{x}+e^{-x}}{e^{x}-e^{-x}}-1\right)\left(\frac{e^{x}+e^{-x}}{e^{x}-e^{-x}}+1\right)\equiv\text{cosech}^{2}{x}$$
$$\left(\frac{e^{x}+e^{-x}}{e^{x}-e^{-x}}-\frac{e^{x}-e^{-x}}{e^{x}-e^{-x}}\right)\left(\frac{e^{x}+e^{-x}}{e^{x}-e^{-x}}+\frac{e^{x}-e^{-x}}{e^{x}-e^{-x}}\right)\equiv\text{cosech}^{2}{x}$$
$$\left(\frac{2e^{-x}}{e^{x}-e^{-x}}\right)\left(\frac{2e^{x}}{e^{x}-e^{-x}}\right)\equiv\text{cosech}^{2}{x}$$
$$\left(\frac{2}{e^{x}-e^{-x}}\right)^2\equiv\text{cosech}^{2}{x}$$
$$\text{cosech}^2{x}\equiv\text{cosech}^{2}{x}$$

> [!Reflection]
> The pattern is the same but the $+$ is changed to a $-$ sign.

## $$\sinh{(\alpha+\beta)}\equiv\sinh{\alpha}\cosh{\beta}+\sinh{\beta}\cosh{\alpha}$$
$$\frac{e^{\alpha+\beta}-e^{-\alpha-\beta}}{2}\equiv\dots$$
$$\frac{e^{\alpha}e^{\beta}-e^{-\alpha}e^{-\beta}}{2}\equiv\dots$$
by applying the process of [[Factorizing a Term and its Reciprocal]]
$$\frac 1 4\left(e^\alpha-\frac 1 {e^\alpha}\right)\left(e^\beta+\frac 1 {e^\beta}\right)+\frac 1 4\left(e^\alpha+\frac 1 {e^\alpha}\right)\left(e^\beta-\frac 1 {e^\beta}\right)\equiv\dots$$
$$\left(\frac{e^\alpha - e^{-\alpha}}2\right)\left(\frac{e^\beta+e^{-\beta}}2\right)+\left(\frac{e^\alpha + e^{-\alpha}}2\right)\left(\frac{e^\beta-e^{-\beta}}2\right)\equiv\dots$$
$$\sinh{\alpha}\cosh{\beta}+\sinh{\beta}\cosh{\alpha}\equiv\dots$$

## $$\sinh{(\alpha-\beta)}\equiv\sinh{\alpha}\cosh{\beta}-\sinh{\beta}\cosh{\alpha}$$
As $\sinh{\beta}$ is an odd function and $\cosh{\beta}$ is an even function^[1],
$$\sinh{(\alpha-\beta)}\equiv\sinh{\alpha}\cosh{\beta}-\sinh{\beta}\cosh{\alpha}$$

## $$\cosh{(\alpha\pm\beta)}=\cosh{\alpha}\cosh{\beta}\pm\sinh{\alpha}\sinh{\beta}$$
By a similar process to above,
$$\cosh{(\alpha\pm\beta)}=\cosh{\alpha}\cosh{\beta}\pm\sinh{\alpha}\sinh{\beta}$$
$$\frac{e^{a+b}+e^{-a-b}}{2}\equiv\dots$$
$$\frac{e^{a}e^{b}+e^{-a}e^{-b}}{2}\equiv\dots$$
By [[Factorizing a Term and its Reciprocal]]
$$\frac12\left[\frac12(e^a+e^{-a})(e^b+e^{-b})+\frac12(e^a-e^{-a})(e^b-e^{-b})\right]\equiv\dots$$
$$\vdots$$
$$=\cosh{\alpha}\cosh{\beta}+\sinh{\alpha}\sinh{\beta}$$



> [!Warning]
> Don't get confused. For normal $\cos(\alpha+\beta)$ double angle rule, the result has inverted signs. I.e.,
> $$\cos(\alpha\pm\beta)=\cos{\alpha}\cos{\beta}\mp\sin{\alpha}\sin{\beta}$$
> Whereas, for a hyperbolic trigonometric function, the signs are the same.
>$$\cosh{(\alpha\pm\beta)}=\cosh{\alpha}\cosh{\beta}\pm\sinh{\alpha}\sinh{\beta}$$

> [!Reflection]
> All of these are results are very similar to that of typical trigonometric functions.

## $$\tanh{\alpha\pm+\beta}\equiv \frac{\tanh \alpha \pm+ \tanh \beta}{1 \pm+ \tanh \alpha \tanh \beta}$$
Derived by a similar process.

## Osborne's Rule
To convert any circular trigonometric identity into a hyperbolic trigonometric identity, follow these two steps:
1. Replace $\sin$ with $\sinh$ and $\cos$ with $\cosh$.
2. Negate term that contains a product of two $\sin$'s (explicit or implicit e.g., $\tan^2$ contains a product of two $\sin$'s).

**Example**
$$\sin{A}\sin{B} \to -\sinh A \sinh B$$
$$\tan^2 A\to - \tanh^2 A$$
$$\cos {2A} = 2\cos^2 A - 1 \to \cosh {2A} = 2\cosh^2 A - 1$$
$$\tan {(A-B)} = \frac {\tan A - \tan B} {1 + \tan A \tan B}\to \tanh {(A-B)} = \frac {\tanh A - \tanh B} {1 - \tanh A \tanh B}$$

> [!Note]
> When faced with an identity problem in the wild you should follow a similar process of solving the problem as you would with non-hyperbolic functions.
>
> **Example**
> $$\sinh{3x}\equiv\text{?}$$
> $$\sin{3x}\equiv\sin{(2x+x)}$$
> $$\equiv\sin{2x}\cos{x}+\sin{x}\cos{2x}$$
> $$\equiv 2\sin{x}\cos^2{x}+\cos^2{x}\sin{x}-\sin^3{x}$$
> $$\equiv 3\sin{x}\cos^2{x}-\sin^3{x}$$
> $$\equiv 3\sin{x}-3\sin^3{x}-\sin^3{x}$$
> $$\equiv 3\sin{x}-4\sin^3{x}$$
> By Osborne's Rule:
> $$\therefore \sinh{3x}\equiv3\sinh{x}+4\sinh^3{x}$$

## Converting $\sinh$ to $\cosh$
$$\sinh x = \frac 3 4$$
$$\space$$
$$\cosh^2 x - \sinh^2 = 1$$
$$\cosh x = \sqrt{1+\sinh^2 x}$$
$$\cosh x = \sqrt{1 + \left(\frac 3 4\right)^2} = \frac 5 4$$
$$\space$$
$$\tanh x = \frac {\sinh x} {\cosh x} = \frac 3 4 \times \frac 4 5 = \frac 3 5$$
$$\space$$
$$\sinh {2x} = 2 \sinh x \cosh x$$
$$= 2 \times \frac 3 4 \times \frac 5 4$$
$$\frac {15} 8$$

# Equations
$$7\space\text{sech}\space x - \tanh x = 5$$
$$7-\sinh x = 5\cosh x$$
$$49-14\sinh x + \sinh^2 x=25 + 25\sinh^2x$$
$$24\sinh^2 x + 14 \sinh x - 24=0$$
$$12\sinh^2 x + 7 \sinh x - 12=0$$
$$\sinh x=\frac {-7\pm25} {24}$$
$$\sinh x = \frac 3 4, \space \sinh x = -\frac {4} 3$$
$$x=\ln{2}, \space x =\ln{\frac 1 3}$$
