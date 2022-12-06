#Maths #FurtherMaths

# Polar Coordinates
---
A polar coordinate can be represented in the form $(r, \theta)$.
> [!Note]
> $\theta$ is always measured anti-clockwise from the horizontal positive axis.


## Converting Cartesian to Polar
$$x=r\cos\theta,\space y=r\sin\theta$$
$$r=\sqrt{x^2+y^2}$$
$$\theta=\arctan{(\frac{y}{x})}$$
> [!Warning]
> The equation $\theta=\arctan{(\frac{y}{x})}$ only works for only the first and fourth quadrant.

**Examples of Converting Cartesian Coordinates to Polar Coordinates**
$$(0,2)\mapsto(2, \frac{\pi}{2})$$
$$(-3,0) \mapsto (3,\pi)$$
$$(1,1) \mapsto (\sqrt{2}, \frac{\pi}{4})$$
$$(-5, 12) \mapsto (13, \pi - \arctan{\frac{12}{5}})$$

## Polar Equation $\to$ Cartesian Equation
**Example 1**
$$r=5$$
$$\sqrt{x^2+y^2}=5$$
$$\implies x^2+y^2=25$$

**Example 2**
![[Pasted image 20220922120258.png|300]]
$$r=2+\cos{2\theta}$$
$$r=2+\cos^2{\theta}-\sin^2{\theta}$$
$$x=r\cos\theta \implies x^2=r^2\cos^2{\theta}\implies\cos^2{\theta}=\frac{x^2}{r^2}$$
$$y=r\sin\theta \implies y^2=r^2\sin^2{\theta}\implies\sin^2{\theta}=\frac{y^2}{r^2}$$
$$\therefore r=2+\frac{x^2}{r^2}-\frac{y^2}{r^2}$$
$$r=2+\frac{1}{r^2}(x^2-y^2)$$
$$\implies \sqrt{x^2+y^2}=2+\frac{x^2-y^2}{x^2+y^2}$$
**Example 3**
![[Pasted image 20220922120232.png|20DD0]]
$$r^2=\sin{2\theta}$$
$$r^2=2\sin{\theta}\cos{\theta}$$

$$x=r\cos\theta \implies \cos{\theta}=\frac{x}{r}$$
$$y=r\sin\theta \implies \sin{\theta}=\frac{y}{r}$$
$$r^2=2\frac{xy}{r^2}$$
$$r^4=2xy$$
$$\implies (x^2+y^2)^2=2xy$$

## Cartesian Equation $\to$ Polar Equation
**Example 1**
$$y^2=4x$$
$$r^2\sin^2{\theta}=4r\cos{\theta}$$
$$r\sin^2{\theta}=4\cos{\theta}$$
$$r=\frac{4\cos\theta}{\sin^2\theta}$$
$$r=4\cot\theta\csc\theta$$
**Example 2**
$$x^2-y^2=5$$

**Example 3**
$$y\sqrt{3}=x+4$$
$$r\sin{\theta}\sqrt{3}=r\cos{\theta}+4$$
$$r(\sqrt{3}\sin\theta-\cos\theta)=4$$
$$r=\frac{4}{\sqrt{3}\sin\theta-\cos\theta}$$
$$\sqrt{3}\sin\theta-\cos\theta=R\sin{(\theta+\alpha)}$$
$$R\sin\theta\cos\alpha+R\sin\alpha\cos\theta$$
$$R\sin\alpha=-1$$
$$R\cos\alpha=\sqrt{3}$$
$$\tan\alpha=-\frac{1}{\sqrt{3}}\implies\alpha=\arctan{-\frac{1}{\sqrt{3}}}=-\frac{\pi}{6}$$ $$R^2=4$$ $$R=2$$
$$\implies r=\frac{2}{\sin{(\theta-\frac{\pi}{6})}}$$

## Sketching Polar Coordinates
We only need to plot the general shape, including interesting points where we move through the intervals of $\pi$. We can do this with a table of values.

**Example 1: $r=a$**

| $\theta$  | $0$ | $\frac{\pi}{4}$ | $\frac{\pi}{2}$ | $\frac{3\pi}{4}$ | $\pi$ | $\frac{5\pi}{4}$ | $\frac{3\pi}{2}$ | $\frac{7\pi}{4}$ | $2\pi$ |
|---|---|---|---|---|---|---|---|---|---|
|  $r$ | $a$ | $a$ | $a$ | $a$ | $a$ | $a$ | $a$ | $a$ | $a$ |
This is a circle, radius $a$.
![[Pasted image 20220922123746.png]]

**Example 2: $\theta=\alpha$**

This is a half line (or a 'ray'). Its origin is at $(0,\alpha)$$ and it extends in only one direction.

E.g. $\theta=\frac{3\pi}{4}$
![[Pasted image 20220922124006.png]]

**Example 3: $r=a\theta$**

| $\theta$ | $0$ | $\frac{\pi}{4}$  | $\frac{\pi}{2}$  | $\frac{3\pi}{4}$  | $\pi$  | $\frac{5\pi}{4}$  | $\frac{3\pi}{2}$  | $\frac{7\pi}{4}$  | $2\pi$  |
| -------- | --- | ---------------- | ---------------- | ----------------- | ------ | ----------------- | ----------------- | ----------------- | ------- |
| $r$      | $0$ | $a\frac{\pi}{4}$ | $a\frac{\pi}{2}$ | $a\frac{3\pi}{4}$ | $a\pi$ | $a\frac{5\pi}{4}$ | $a\frac{3\pi}{2}$ | $a\frac{7\pi}{4}$ | $a2\pi$ |
![[Pasted image 20220922124344.png]]

**Example 4: $r=a(1+\cos\theta)$**

| $\theta$ | $0$  | $\frac{\pi}{4}$                | $\frac{\pi}{2}$ | $\frac{3\pi}{4}$        | $\pi$ | $\frac{5\pi}{4}$        | $\frac{3\pi}{2}$ | $\frac{7\pi}{4}$        | $2\pi$ |
| -------- | ---- | ------------------------------ | --------------- | ----------------------- | ----- | ----------------------- | ---------------- | ----------------------- | ------ |
| $r$      | $2a$ | $a\frac{1+\sqrt{2}}{\sqrt{2}}$ | $a$             | $a\frac{2-\sqrt{2}}{2}$ | $0$   | $a\frac{2-\sqrt{2}}{2}$ | $a$              | $a\frac{2+\sqrt{2}}{2}$ | $2a$   |

**Empty Table**

| $\theta$ | $0$ | $\frac{\pi}{4}$ | $\frac{\pi}{2}$ | $\frac{3\pi}{4}$ | $\pi$ | $\frac{5\pi}{4}$ | $\frac{3\pi}{2}$ | $\frac{7\pi}{4}$ | $2\pi$ |
| -------- | --- | --------------- | --------------- |:---------------- | ----- | ---------------- | ---------------- | ---------------- | ------ |
|          |     |                 |                 |                  |       |                  |                  |                  |        |

## Integrating Polar Graphs
$$\frac{1}{2}\int\limits^\beta_\alpha{r^2}{d\theta}$$
To [[Integration|integrate]] between two angles $\alpha$ and $\beta$, we take the sum of all the infinitesimally small sectors with angle $d\theta$.
![[Pasted image 20220926115547.png]]
Each sector has an area $\frac{1}{2}r^2d\theta$. Therefore, the sum of all the sectors is equal to $\frac{1}{2}\int\limits^\beta_\alpha{r^2}{d\theta}$.

> [!Note]
> Take advantage of symmetry where possible.

> [!Note]
> Sometimes a question may ask something along the lines of $\text{Find the area of one loop of the polar rose}$ $r=a\sin 4\theta$. In such case, the angles ([[Integration#Limits|limits]]) are not explicitly stated, therefore, a sketch must drawn of the function.

> [!Tip]
> These identities come up very often. It is worth memorizing them. (Derived from [[Double Angle Identities]])
> $$\cos^2{x}=\frac{1}{2}+\frac{1}{2}\cos{2x}$$
> $$\sin^2{x}=\frac{1}{2}-\frac{1}{2}\cos{2x}$$


**Example 1**
Find the area enclosed by the cardioid $r=a(1+\cos\theta)$
![[Pasted image 20220926120024.png]]
$$\text{Area}=\frac{1}{2}\int\limits^{2\pi}_0{a^2(1+\cos\theta)^2}{d\theta}$$
By symmetry,
$$=\int\limits^\pi_0{a^2(1+\cos\theta)^2}{d\theta}$$
$$=a^2\int\limits^\pi_0{(1+\cos\theta)^2}{d\theta}$$
$$=a^2\int\limits^\pi_0{(1+2\cos\theta+\cos^2\theta)}\space{d\theta}$$
$$=a^2\int\limits^\pi_0{(1+2\cos\theta+\frac{1}{2}+\frac{1}{2}\cos2\theta)}\space{d\theta}$$
$$=a^2[\frac{3}{2}\theta-2\sin\theta-\frac{1}{4}\sin {2\theta}]^\pi_0$$
$$\vdots$$
$$\text{Area}=a^2\frac{3\pi}{2}$$

### Area Between Two Curves
Given two curves $r_1=f(\theta)$ and $r_2=g(\theta)$
$$\text{Area between curves}=\frac{1}{2}\left(\int\limits^\beta_\alpha{f(x)^2}\space{d\theta}-\int\limits^\beta_\alpha{g(x)^2}\space{d\theta}\right)$$
$$=\frac{1}{2}\int\limits^\beta_\alpha{(f(x)^2-g(x)^2)}\space{d\theta}$$
> [!Tip]
> The challenge when solving questions related to finding the area between two curves is finding the intersection of the two curves. *Sketching a diagram is usually a helpful method*.

> [!Warning]
> Sometimes the area is not the difference between two curves but rather the composite of two different curves between different bounds.
> $$\text{composite area}=\frac{1}{2}\left(\int\limits^\beta_\alpha{r^2_1}\space d\theta+\int\limits^\gamma_\beta{r^2_2}\space d\theta\right)$$



**Example**

Find the exact value of the area bound by the curves $r_1=2+\cos\theta$ and $r_{2} = 5\cos\theta$.

Step 1: Sketch the curves.
> [!Warning]
> The values $\alpha$ and $\beta$ are not necessarily the points of intersection are not necessarily the points of intersection.

![[Pasted image 20220926123619.png]]

Step 2: Identify bounds.
> [!Note]
> As we are integrating inside both curves, we will split the regions into $A^{\frac{\pi}{2}}_{\alpha}$ and $B^{\alpha}_{0}$.
> 
> Region $A$ is entirely composed of $r_2$ and region $B$ is entirely composed of $r_1$. 
> 
> Here symmetry is being taken advantage of.

To calculate $\alpha$, 
$$2+\cos\theta=5\cos\theta$$
$$2=4\cos\theta$$
$$\theta=\arccos\frac{1}{2}=\frac{\pi}{3}$$

Step 3: Integrate.
$$\text{Area}=\int\limits^\frac{\pi}{2}_\frac{\pi}{3}{25\cos^2\theta \space d\theta}+\int\limits^{\frac{\pi}{3}}_{0}(4+4\cos\theta+\cos^2\theta) \space d\theta$$
$$=\int\limits^\frac{\pi}{2}_\frac{\pi}{3}{25\cos^2\theta \space d\theta}+\int\limits^{\frac{\pi}{3}}_{0}(4+4\cos\theta+\frac{1}{2}+\frac{1}{2}\cos 2\theta) \space d\theta$$
$$=\left[\frac{25}{2}\theta+\frac{25}{4}\sin2\theta\right]^\frac{\pi}{2}_\frac{\pi}{3}+\left[\frac{9}{2}\theta+4\sin\theta+\frac{1}{4}\sin 2\theta\right]^\frac{\pi}{3}_0$$
$$\vdots$$
$$\text{Area}=\frac{43\pi}{12}-\sqrt{3}$$

## Tangents and Normals
Because, $x=r\cos\theta$ and $y=r\sin\theta$,

When the gradient line is vertical:
$$\frac{dx}{d\theta}=0$$
When the gradient line is horizontal:
$$\frac{dy}{d\theta}$$

**Example**
A curve has polar equation:
$$r=1+2\cos\theta,\space 0\le\theta\le\frac{\pi}{2}$$
At point $P$, the tangent to the curve is parallel to the initial line. Given that $O$ is the pole, find the exact length of the line $OP$. Also, find the equation of this tangent line.
$$y=r\sin\theta$$
$$y=\sin\theta(1+2\cos\theta)$$
$$y=\sin\theta+2\sin\theta\cos\theta$$
$$\frac{dy}{d\theta}=\cos\theta+2\cos{2\theta}$$
$$\cos\theta+2\cos2\theta=0$$
$$\cos\theta+2\cos^2\theta-2\sin^2\theta=0$$
$$\cos\theta+2\cos^2\theta-2+2\cos^2\theta=0$$
$$4\cos^2\theta+\cos\theta-2=0$$
$$\cos\theta=\frac{=1\pm\sqrt{1-4\times4\times(-2)}}{8}$$
$$\theta=\arccos{\frac{-1+\sqrt{1+32}}{8}}$$
Here $\theta=\arccos{\frac{-1+\sqrt{1+32}}{8}}$ represents the angle at which the tangent to the curve at that angle is parallel to the initial line.
$$\implies |OP|=\frac{3+\sqrt{33}}{4}$$

To find the tangent: we know the line will of the form $y=k$, so we can use the values of $(r, \theta)$ to find the values of $y$. 
$$y=r\sin\theta$$
$$\frac{3+\sqrt{33}}{4}\sin(\arccos{\frac{-1+\sqrt{33}}{8}})\approx 1.76$$
$$r={1.76}\div{\sin\theta}$$
