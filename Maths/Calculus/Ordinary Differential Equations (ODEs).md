> [!Definition]
> An **equation** is a set of expressions that are equal to each other.

> [!Definition]
> A **differential** is measuring the derivative of a function.

> [!Definition]
> **Ordinary** means the order relating to the thing.
> In this case, the orders will be measured of the differential and formed into an equation.

> [!Definition]
> **Linear**
> 
> All the derivatives must be linear terms, i.e., none of the terms can be squared or multiplied together,

> [!Definition]
> **Homogeneous**
>
> A homogeneous differential equation is one where:
> $$\text{RHS}=0$$

> [!definition]
> **Constant Coefficient**
> All the coefficients are constants.

> [!Definition]
> **Particular Integral**
>
> Any single solution to an ODE is called a particular integral. For our study this is generally used in reference to in-homogeneous equations for a solution that generates the $RHS$.

> [!Definition]
> **Complementary Function**
> 
> The solution to an associated homogeneous ODE.

# FODEs (Integrating Factor Problems)

**First Order Differential Equations**

I.e., the highest order of derivative will be the first derivative.

Most of the FODEs in this chapter will take the form $\frac{dy}{dx}+Py=Q$ (where $P$ and $Q$ are functions of $x$)

Generally speaking, all of these FODEs will be solvable via the *reverse product rule*.

> [!Note to self]
> **Reverse Product Rule**
>
> We would like to take the derivative of $u\times v$
> 
> Using the product rule: $u'v+uv'$
>
> To use the reverse product rule: 
> - $u=y, u'=\frac {dy}{dx}$
> - $v\frac{dy}{dx}+v'y=[vy]'$

> E.g., find the general solutions of the equations $x^3 \frac{dy}{dx}+3x^2y=\sin{x}$
> 
> By **reverse product rule**:
> $$\frac{d[x^3y]}{dx}=\sin x$$
> $$d[x^3y]=\sin x \ dx$$
> $$\int d[x^3y]=\int \sin x \ dx$$
> $$x^3y=-\cos{x} + C$$
> $$y=\frac{-\cos{x}+C}{x^3}$$

> [!Example]
> Find general solutions of the equation $\frac1x\frac{dy}{dx}-\frac1{x^2}y=e^x$
> $$\frac{d[\frac{y}{x}]}{dx}=e^x$$
> $$\int d\left[\frac{y}{x}\right]=\int e^x\ dx$$
> $$\frac{y}{x}=e^x+C$$
> $$y=x(e^x+C)$$

> [!Example]
> Find general solutions of the equation $4xy\frac{dy}{dx}+2y^2=x^2$
> $$\frac{d[2xy^2]}{dx}=2(y^2+2xyy')$$
> $$\frac{d[2xy^2]}{dx}=x^2$$
> $$d[2xy^2]=x^2dx$$
> $$\int d[2xy^2]=\int x^2dx$$
> $$2xy^2=\frac13x^3+C$$
> $$y^2=\frac16x^2+\frac{C}{2x}$$
> $$y=\sqrt{\frac16x^2+\frac{C}{2x}}$$

## What to do if a FODE cannot be immediately expressed as a product.
> [!Example]
> Find the general solution of $\frac{dy}{dx}-4y=e^x$
> 
> To do this, we must multiply through by an integrating factor that is an unknown function of $x$.
> $$I\frac{dy}{dx}-4Iy=Ie^x$$
> $I$ needs to be such that $\frac{dI}{dx}=-4I$. Thus, we chose:
> $$I=e^{-4x}$$
> $$e^{-4x}\frac{dy}{dx}-4e^{-4x}y=e^{-4x}e^x$$
> This then allows us to use the reverse product rule.
> $$\frac{d[e^{-4x}y]}{dx}=e^{-4x}e^x$$
> $$d[e^{-4x}y]=e^{-4x}e^xdx$$
> $$\int d[e^{-4x}y]=\int e^{-4x}e^xdx$$
> $$e^{-4x}y=-\frac13e^{-3x} + C$$
> $$y=-\frac13e^{x} + Ce^{4x}$$

## General Case
Find the general solution of 
$$\frac{dy}{dx}+Py=Q$$
where $P$ and $Q$ are functions of $x$.

There is no immediate reverse product on the LHS. Therefore, we must multiply through by an integrating factor. Let us assume that $f(x)$ is a valid integrating factor.

$$f(x)\frac{dy}{dx}+f(x)Py=f(x)Q$$

$$\frac{d[fy]}{dx}=f(x)\frac{dy}{dx}+f'(x)y=f(x)Q$$
We need to find $f(x)$ such that $f(x)P=f'(x)$.
> [!Aside]
> How do we find $f(x)$ such that $f(x)P=f'(x)$?
> $$f(x)P(x)=\frac{d f(x)}{dx}$$ 
> $$f(x)P(x)dx=df(x)$$
> $$P(x)dx=\frac{1}{f(x)}df(x)$$
> $$\int P(x)dx=\int \frac{1}{f(x)}df(x)$$
> > Any of these family of solutions will work, therefore we pick the simples one (where the $C=0$ [$+C$ is omitted]).
>
> $$\int P(x)dx=\ln {f(x)}$$
> $$e^{\int P(x)dx}=f(x)$$

$$e^{\int P(x)dx}\frac{dy}{dx}+e^{\int P(x)dx}Py=e^{\int P(x)dx}Q$$
$$\frac{d[e^{\int Pdx}\times y]}{dx}=e^{\int P(x)dx}Q$$
$$d[e^{\int Pdx}\times y]=e^{\int P(x)dx}Qdx$$
$$\int d[e^{\int Pdx}\times y]=\int e^{\int P(x)dx}Q\ dx$$
$$\vdots$$
$$y=\frac{\int[e^{\int P \ dx}\times Q]dx}{e^{\int P \ dx}}$$
For all linear, first order, differential equations of the form $y'+Py = Q$, an integrating factor of $e^{\int P dx}$ can be used to convert the LHS into a reverse product.

> [!Example]
> Find the general solution of $\cos{x}\frac{dy}{dx}+2y\sin{x}=cos^4{x}$
> > [!Warning]
> > The coefficient of $\frac{dy}{dx}$ must be $1$
> 
> Thus, we divide all terms by $\cos{x}$
> $$\frac{dy}{dx}+2\tan{x}\times y=\cos^3{x}$$
> $$\vdots$$
> $$\frac{d[\sec^2{x}\times y]}{dx}=\cos{x}$$
> $$\int d[\sec^2{x}\times y] = \int \cos{x} \ dx$$
> $$ysec^2{x}=\sin{x}+C$$
> $$y=\cos^2{x}(\sin{x}+C)$$

## Constant Coefficient Linear Homogeneous FODE
$$ay'+by=0$$
$$y'+\frac{b}{a}y=0$$
$$\frac{d[e^{x\frac{b}{a}}\times y]}{dx}=0$$
$$d[e^{x\frac{b}{a}}\times y]=0\times dx$$
$$\int d[e^{x\frac{b}{a}}\times y]=\int 0 \times dx$$
$$y\times e^{x\frac{b}{a}}=C$$
$$y=Ce^{-x\frac{b}{a}}$$


# SODEs (homogeneous, constant coefficient, linear)

**Second Order Differential Equation**

$$ay'' + by' + cy = 0$$
where:
* $a$, $b$ and $c$ are constant

We saw in the constant coefficient, homogenous, linear FODE a general solution existed in the format $y=Ae^{mx}$. Let us assume that a similar solution would exist for a SODE and further, let us assume that it takes the same form.

$$y=Ae^{mx}$$
$$y'=Ame^{mx}$$
$$y''=Am^2e^{mx}$$

Now substitute:
$$ay'' + by' + cy = 0$$
$$\downarrow$$
$$aAm^2e^{mx}+bAme^{mx}+cAe^{mx}=0$$
$$Ae^{mx}( am^2+bm+c )=0$$
assume $Ae^{mx}\neq0$ 
$$\therefore am^2+bm+c = 0$$

> [!Definition]
> **Auxiliary Equation of $$ay''+by'+cy=0$$ is:**
> $$am^2+bm+c = 0$$
> $$m=\frac{-b\pm\sqrt{b^2-4ac}}{2a}$$

From the auxiliary equation, the value of $m$ can be found. This constitutes the general solution to the second order differential equation.

The auxiliary solution will always have $2$ results, therefore our general solution must be of the form:

$$y = Ae^{m_1x}+Be^{m_2x}$$

The linear combination of any individual solution will always produce a solution.

## Validation
$$\text{let}\ y = Ae^{m_1x}+Be^{m_2x}$$
thus,
$$y'=m_1Ae^{m_1x}+m_2Be^{m_2x}$$
$$y''=m_1^2Ae^{m_1x}+m_2^2Be^{m_2x}$$
and substituting into $ay'' + by' + cy = 0$:
$$a(m_1^2Ae^{m_1x}+m_2^2Be^{m_2x})+b(m_1Ae^{m_1x}+m_2Be^{m_2x})+c(Ae^{m_1x}+Be^{m_2x})=0$$
$$Ae^{m_1x}(am_1^2+bm_1+c)+Be^{m_2x}(am_2^2+bm_2+c)=0$$

By definition $m_1$ and $m_2$ will yield zero in the quadratic terms.

Therefore, the $LHS$ must equal $0$. Thus, it is a valid solution.

> [!Summary]
> * Take a constant coefficient, homogeneous, linear SODE.
> * Convert the coefficients into the auxiliary equation.
> * Where the equation has two distinct real roots, the solution must be $Ae^{\alpha x}+Be^{\beta x}$

Find the general solution of the equation $2y''+5y'+3y=0$
$$\vdots$$
$$\alpha,\beta=\frac{-5\pm1}{2}$$
$$\alpha=-1,\ \beta=-\frac{3}{2}$$
$$y=Ae^{-x}+Be^{-\frac32 x}$$

## Auxiliary Equation with $1$ Distinct Real Root.
$$ay'' + by' + cy = 0$$
Consider the auxiliary equation $am^2 + bm + c = 0$.

Let $b^2-4ac=0$. Thus, $m=\frac{-b}{2a}$.

$$y=Ae^{-\frac{b}{2a}x}+Be^{-\frac{b}{2a}x}$$
can be written *w.l.o.g.* as $y=Ke^{-\frac{b}{2a}x}$

> [!Danger]
> We've lost information here.

Assume, for a new line of enquiry, $y=Axe^{mx}$
#Todo derivation

Following the same derivation as above, this will also yield a solution. Therefore, the general solution will be the linear combination.

The general solution is:

$$y=(A+Bx)e^{\alpha x}$$

> [!Example]
> Find the general solution of $y'' - 6y' +9y = 0$
> 
> by auxiliary equation:
> $$m=\frac{6\pm\sqrt{36-36}}{2}=3$$
> 
> > [!Tip]
> > To gain **ALL MARKS** on the test:
> >
> > ✅Write out the auxiliary equation ($am^2+bm+c=0$)✅
> 
> Because, $m$ has one solution, the answer must be:
> 
> $$ y = (A+Bx)e^{3x}$$

## Auxiliary Equation with $0$ Real Roots.
Consider a second order, constant coefficient, homogeneous, linear differential equation
$$ay'' + by' + cy = 0$$
such that the auxiliary equation $am^2+bm+c=0$ yields the complex root $m=\lambda \pm i\mu$

$$y=Ae^{(\lambda + i\mu)x} + Be^{(\lambda - i\mu)x}$$
factorise (take out factor $e^{\lambda x}$):
$$y=e^{\lambda x}(Ae^{i\mu x} + Be^{-i\mu x})$$
using [[Complex Numbers#Euler's Theorem|Euler's theorem]] we can rewrite $e^{i \mu x}$ as $\cos x\mu + i\sin x\mu$

$$e^{\lambda x}\left[ A[\cos x\mu + i\sin x\mu] + B[\cos (-x\mu) + i\sin (-x\mu)] \right]$$

$$=e^{\lambda x}\left[ A[\cos x\mu + i\sin x\mu] + B[\cos x\mu - i\sin x\mu] \right]$$
$$=e^{\lambda x}\left[ (A+B)\cos x \mu + (A-B)i\sin x\mu \right]$$
$$=e^{\lambda x}\left[ P\cos x \mu + Q\sin x\mu \right]$$

### Validation
Assume that 
$$y=e^{\lambda x}\left [ P \cos \mu x + Q \sin \mu x \right ]$$
is the general solution to
$$ay'' + by' + cy = 0$$
so now we calculate the first derivative.
$$y' = \lambda e^{\lambda x} \left [ P \cos \mu x + Q \sin \mu x\right ] + e^{\lambda x}[-P\mu \sin \mu x + Q \mu \cos \mu x ]$$
and the second derivative.
$$y'' = \lambda^2 e ^{\lambda x}[P\cos \mu x + Q \sin \mu x] + 2\lambda e^{\lambda x}[-P\mu \sin \mu x + Q\mu \cos \mu x] + e^{\lambda x} [-P\mu^2\cos \mu x - Q\mu^2 \sin \mu x]$$

$y''$ $y'$ and $y$ all have a factor of $e^{\lambda x}$. Given that $e^{\lambda x} \neq 0$, we can comfortably divide the ODE by $e^{\lambda x}$, and, thus, ignore it in our substitution.


$$y=\left [ P \cos \mu x + Q \sin \mu x \right ]$$
$$y' = \lambda\left [ P \cos \mu x + Q \sin \mu x\right ] + [-P\mu \sin \mu x + Q \mu \cos \mu x ]$$
$$y'' = \lambda^2[P\cos \mu x + Q \sin \mu x] + 2\lambda [-P\mu \sin \mu x + Q\mu \cos \mu x] + [-P\mu^2\cos \mu x - Q\mu^2 \sin \mu x]$$

$$\sin\mu x \left [ 
a(\lambda^2 Q - 2\lambda\mu P -  \mu^2 Q)
+ b(\lambda Q -\mu P)
+ cQ
\right]$$

$$\cos \mu x \left [
a(\lambda^2P+2\lambda\mu Q-\mu^2P)+b(\lambda P+\mu Q)+cP
\right]$$

> [!Note to self]
> I have no idea what I'm doing. ✏️
> I.e., splitting into factors of $P \sin$, $P \cos$, $Q \sin$ and $Q \cos$.

$$Q\sin\mu x \left [ 
a(\lambda^2  -  \mu^2 )
+ b(\lambda )
+ c
\right]$$
$$+$$
$$P\sin\mu x \left [ 
a(- 2\lambda\mu )
+ b(-\mu )
\right]$$
$$+$$
$$Q\cos \mu x \left [
a(2\lambda\mu )+b(\mu )
\right]$$
$$+$$
$$P\cos \mu x \left [
a(\lambda^2-\mu^2)+b(\lambda )+c
\right]=0$$

> [!Aside]
> Consider the auxiliary equation $am^2 + bm + c = 0$
> $$m = \frac{-b \pm \sqrt { b^2 - 4ac }} { 2a }$$
> $$m=\frac {-b} {2a} \pm i \frac{\sqrt{4ac - b^2}}{2a}$$
> $$m = \lambda \pm i\mu$$
> $$\lambda = - \frac {b} {2a},\ \ \ \mu = \frac{\sqrt{4ac - b^2}}{2a}$$

By substituting $\lambda$ and $\mu$ in terms of $a$, $b$ and $c$ into the $4$ terms, it is shown that they all equate to $0$, thus making the equation true.

**$1^{\text{st}}$ Term**
$$Q\sin\mu x \left [ 
a(\lambda^2  -  \mu^2 )
+ b(\lambda )
+ c
\right]$$

$$Q\sin\mu x \left [ 
a(\frac {b^2} {4a^2}  -  
\frac{4ac - b^2}{4a^2}
)
- \frac{b^2}{2a}
+ c
\right]$$

$$Q\sin\mu x \left [ 
  
\frac{2b^2 - 4ac}{4a}

- \frac{2b^2}{4a}
+ \frac{4ac}{4a}

\right] = 0$$
Success ✅

**$2^{\text{nd}}$ Term**
$$P\sin\mu x \left [ 
a(- 2\lambda\mu )
+ b(-\mu )
\right]$$
$$\vdots$$
$$P\sin\mu x \left [ 
\frac{b\sqrt{4ac-b^2}}{2a}
- \frac{b\sqrt{4ac-b^2}}{2a}
\right]$$

**$3^{\text{rd}}$ & $4^{\text{th}}$ Term**
<br/>
Are symmetrically equivalent to the $1^{\text{st}}$ and $2^{\text{nd}}$ terms.

# SODEs (in-homogeneous, constant coefficient, linear)
$$ay'' + by' + cy = f(x)$$
> [!Warning]
> If $f(x)=0$, this is SODE is [[#SODEs (homogeneous, constant coefficient, linear)|homogeneous]].

Assume there exists a solution $y_0$.
If we substitute $y_0$, $y_0'$ and $y_0''$ into the $LHS$, then we would get $f(x)$.

$$f(x)+0=f(x)$$
Assume there exits a solution $y_1$ which solves the associated homogeneous SODE (where $RHS = 0$). Substituting $y_1$ and its derivatives into the associated homogeneous would yield $0$. Thus, substituting $y_0 + y_1$ into the SODE, will yield $f(x) + 0$ and is therefore a valid solution.

We will call $y_0$ the **particular integral**.

We will call $y_1$ the **complimentary function**.

And, therefore, the general solution to the in-homogeneous SODE will the sum of the particular integral and complimentary function. 

> [!374]
> I will be abbreviating complimentary function to CF and particular integral to PI.

- In order to find the PI, consider a function that is of the same type as $f(x)$.

> [!Example]
> **$f(x) = \text{constant}$**
> $$y'' - 5y' + 6y = 3$$
> $$f(x) \text{ is a constant} \therefore PI \text { should be a constant}$$
> $$PI = \lambda$$
> $$y=\lambda$$
> $$y'=0$$
> $$y''=0$$
> substituting into the differential equation:
> $$\rightarrow 0 - 5(0) + 6\lambda = 3$$
> $$\lambda = \frac12 \implies PI=\frac12$$
> Therefore, the general solution is:
> $$y=\frac12 + Ae^{2x}+Be^{3x}$$

> [!Example]
> $$y''- 5y' + 6y = 2x$$
> $f(x)$ is linear, so $PI = \lambda x + \mu$
> $$y = \lambda x + \mu$$
> $$y' = \lambda$$
> $$y'' = 0$$
> substituting into the differential equation:
> $$-5\lambda + 6\lambda x + 6\mu = 2x$$
> by comparing coefficients
> $$-5\lambda+6\mu=0, \ \ 6\lambda=2$$
> $$\lambda = \frac13$$
> $$\rightarrow \mu=\frac5{18}$$
> Therefore, the general solution is:
> $$y=\frac13 x + \frac{5}{18} + Ae^{2x}+Be^{3x}$$

## Cheat-sheet for choosing a particular integral.
![[Pasted image 20230111130446.png]]

> [!Warning]
> We cannot use a particular integral that is part of the complementary function as this would yield $0$.
>
> > **Solution**
> > 
> > Stick an $x$ in front and get on with your day.
> 
> > [!Example]
> > $$y'' - 5y' + 6y = e^2x$$
> > The complimentary function is $Ae^{2x} + Be^{2x}$, therefore the particular integral would have to be of the format $\lambda x e^{2x}$

# ODEs (by substitution)
Using a substitution method we can, sometimes, convert a non-linear ODE into a format that we can solve.

* Non-Linear FODE -> integrating factor method / separable variables
* Non-Linear SODE -> constant coefficient

> [!Tip]
> In an exam, you will know its a substitution problem because it will say "use the substitution." The method is to calculate derivatives, substitute and rearrange.

> [!Example]
> **Example 1 (FODE)**
>
>  Use the substitution $z=\frac y x$ to transform the differential equation $\frac{dy}{dx}=\frac{x^2+3y^2}{2xy}, x\gt0$ into a differential equation in $z$ and $x$. By first solving this new equation, find the general solution of the original equation giving $y^2$ in terms of $x$.
> $$y=xz$$
> $$\frac{dy}{dx}=xz'+z$$
> Substituting the terms in.
> $$xz'+z=\frac{x^2+3x^2z^2}{2x^2z}$$
> Simplifying and separating the variables.
> $$xz'+z=\frac{1+3z^2}{2z}$$
> $$2xzz'+2z^2=1+3z^2$$
> $$2xzz'=1+z^2$$
> $$xz'=\frac{1+z^2}{2z}$$
> $$x\frac{dz}{dx}=\frac{1+z^2}{2z}$$
> $$x\frac{1}{dx}=\frac{1+z^2}{2z}\frac{1}{dz}$$
> $$\frac{1}{x}dx=\frac{2z}{1+z^2}dz$$
> $$\int\frac{1}{x}dx=\int\frac{2z}{1+z^2}dz$$
> $$\ln x = \ln {\left(1+z^2 \right)}+\ln C$$
> $$\ln x = \ln {\left(C+Cz^2 \right)}$$
> $$e^{\ln x} = e^{\ln {\left(C+Cz^2 \right)}}$$
> $$x = C+Cz^2$$
> Substitute $z=\frac{y}{x}$  back in again.
> $$x=C+C\frac{y^2}{x^2}$$
> $$x^3-Cx^2=Cy^2$$
> $$y^2=\frac{x^3-Cx^2}{C}$$

> [!Example]
> **Example 2 (FODE -> integrating factor)**
> 
> Use the substitution $z=y^{-1}$ to transform the differential equation $\frac{dy}{dx}+xy=xy^2$, into a differential equation in $z$ and $x$. Find the general solution using an integrating factor.
> 
> $$y=z^{-1}$$
> $$\frac{dy}{dx} = -z'z^{-2}$$
> Substitute
> $$-z'z^{-2}+xz^{-1}=xz^{-2}$$
> $$-z'+xz=x$$
> $$z'-xz=-x$$
> By integrating factor:
> $$e^{\int P(x)dx}=f(x)$$
> $$P(x)=-x$$
> $$e^{\int -x \ dx}=f(x)$$
> $$e^{-\frac{1}{2}x^2}=f(x)$$
> $$e^{-\frac12 x^2}z'-xze^{-\frac12 x^2}=-xe^{-\frac12 x^2}$$
> $$\text{LHS}=\frac{d\left[e^{-\frac{1}{2}x^2}\times z\right]}{dx}$$
> $$\frac{d\left[e^{-\frac{1}{2}x^2}\times z\right]}{dx}=-xe^{-\frac12 x^2}$$
> $$d\left[e^{-\frac{1}{2}x^2}\times z\right]=-xe^{-\frac12 x^2}dx$$
> $$\int d\left[e^{-\frac{1}{2}x^2}\times z\right]=\int-xe^{-\frac12 x^2}dx$$
> $$e^{-\frac{1}{2}x^2}\times z=\int-xe^{-\frac12 x^2}dx$$
> $$e^{-\frac{1}{2}x^2}\times z=e^{-\frac{1}{2}x^2}+C$$
> $$z=\frac{e^{-\frac{1}{2}x^2}+C}{e^{-\frac{1}{2}x^2}}$$
> $$z=1+Ce^{\frac12 x^2}$$
> $$y^{-1}=1+Ce^{\frac12 x^2}$$
> $$y=\frac{1}{1+Ce^{\frac12 x^2}}$$

**Example 3 (SODE -> constant coefficient)**

Use the substitution $x=e^u$ (to obtain an equation involving $y$ and $u$), solve the differential equation $x^2 \frac{d^2y}{dx^2}+x\frac{dy}{dx}+y=0$

Find what $\frac{dy}{dx}$ is and $\frac{d^2y}{dx^2}$ is so we can substitute them in our differential equation.

$$\frac{dx}{du}=e^u$$
$$\frac{du}{dx}=\frac1x$$
$$\frac{dy}{dx}=\frac{dy}{du}\times\frac{du}{dx}=\frac{dy}{du}\times\frac1x$$
$$\frac{d^2y}{dx^2}=\frac{d[\frac{dy}{du}e^{-u}]}{du}\frac{du}{dx}=\frac{d[\frac{dy}{du}e^{-u}]}{du}e^{-u}$$
$$\frac{d^2y}{dx^2}=\frac1x\left(\frac{d^2y}{du^2}\frac1x-\frac{dy}{du}\frac1x\right)$$
$$\frac{d^2y}{dx^2}=\frac1{x^2}\left(\frac{d^2y}{du^2}-\frac{dy}{du}\right)$$
Substitute:
$$\left(\frac{d^2y}{du^2}-\frac{dy}{du} \right)+\frac{dy}{du}+y=0$$
$$\frac{d^2y}{du^2}+y=0$$
$$\vdots$$
$$y=A\sin(u)+B\cos(u)$$
Converting back into an equation in terms of $x$:
$$y=A\sin(\ln{x})+B\cos(\ln{x})$$