```ad-recall
**Kinematic equations of motion**
(also remember, acceleration is assumed to be constant)
$$\frac{dv}{dt}=a$$
$$\implies v=u+at$$
\
$$s=\int v\ dt$$
$$\implies s=ut+\frac12at^2$$
\
$$\frac{ds}{dt}=v$$
$$\implies s=\frac{(v+u)}{2}t$$

by rearranging (i think),
$$v^2=u^2+2as$$
```

```ad-note
It will be assumed that upwards is the positive direction and downwards is the negative direction. Therefore, acceleration, $g$, is
$$g=-10\ ms^{-1}$$

Horizontal acceleration will be assumed to be $0$.
```

```ad-example
A particle is project horizontally at $25\ ms^{-1}$ from a point $78.4$ metres above a horizontal surface. Find: 

(a) the time taken by the particle to reach the surface.
(b) the horizontal distance travelled in that time. 
(c) the distance of the impact point from the original point.

$$r_0=\left(\begin{matrix}0\\78.4\end{matrix}\right)$$
$$u=\left(\begin{matrix}25\\0\end{matrix}\right)$$
$$a=\left(\begin{matrix}0\\-10\end{matrix}\right)$$
$$t=t$$
\
$$r=r_0+s$$
$$r=r_0+\left[ut+\frac12at^2\right]$$
$$\left(\begin{matrix}x\\0.0\end{matrix}\right)=\left(\begin{matrix}0.0\\78.4\end{matrix}\right)+\left[\left(\begin{matrix}25.0\\0.0\end{matrix}\right)t+\frac12\left(\begin{matrix}0.0\\-10.0\end{matrix}\right)t^2\right]$$
$$\left(\begin{matrix}x\\0.0\end{matrix}\right)=\left(\begin{matrix}25t\\78.4-5t^2\end{matrix}\right)$$
thus,
$$t=\sqrt{\frac{78.4}{5}}=3.9598\ s$$
$$x=70\sqrt{2}\approx98.995\ m$$
$$r_1=\left(\begin{matrix}98.995\\0\end{matrix}\right)$$
this yields
$$\left|r_1-r_0\right|=\left|\left(\begin{matrix}98.995\\-78.4\end{matrix}\right)\right|=126.3\ m$$




```

```ad-example
A particle is projected horizontally with a speed of $U\ ms^{-1}$ from a point of $122.5\ m$ above a horizontal plane. The particle hits the plan at a point which is at a horizontal distance of $90\ m$ away from the starting point. Find the initial speed of the particle.

$$r_0=\left(\begin{matrix}0.0\\122.5\end{matrix}\right)$$
$$r_1=\left(\begin{matrix}90\\0\end{matrix}\right)$$
$$s=\left(\begin{matrix}90\\-122.5\end{matrix}\right)$$
$$u=\left(\begin{matrix}U\\0\end{matrix}\right)$$
$$a=\left(\begin{matrix}0\\-10\end{matrix}\right)$$
$$t=t$$
$$s=ut+\frac12at^2$$
$$\left(\begin{matrix}90\\-122.5\end{matrix}\right)=\left(\begin{matrix}U\\0\end{matrix}\right)t+\frac12\left(\begin{matrix}0\\-10\end{matrix}\right)t^2$$
$$\left(\begin{matrix}90\\-122.5\end{matrix}\right)=\left(\begin{matrix}Ut\\-5t^2\end{matrix}\right)$$
$$-5t^2=-122.5\implies t=\frac{7\sqrt{2}}{2}\approx4.95\ s$$
$$90=Ut\implies U\approx18.2\ ms^{-1}$$
```

```ad-example
**Not only is it horizontal motion example**
A particle $𝑃$ is projected from a point $𝑂$ on a horizontal plane with speed $28\ ms^{-1}$ and with angle of elevation $30°$. After projection, the particle moves freely under gravity until it strikes the plane at a point $𝐴$. Find: the greatest height above the plane reached by $𝑃$ the time of flight of $𝑃$ the distance $𝑂𝐴$

$$r_0=\left(\begin{matrix}0\\0\end{matrix}\right)$$
$$r_1=\left(\begin{matrix}A\\0\end{matrix}\right)$$
$$u=\left(\begin{matrix}28\cos30\\28\sin30\end{matrix}\right)$$
$$=\left(\begin{matrix}14\sqrt{3}\\14\end{matrix}\right)$$
$$a=\left(\begin{matrix}0.0\\-10.0\end{matrix}\right)$$
$$t=t$$
$$s=ut+\frac12at^2$$
$$\left(\begin{matrix}A\\0\end{matrix}\right)=\left(\begin{matrix}14\sqrt{3}\\14\end{matrix}\right)t+\frac12\left(\begin{matrix}0.0\\-10.0\end{matrix}\right)t^2$$
$$\left(\begin{matrix}A\\0\end{matrix}\right)=\left(\begin{matrix}(14\sqrt{3})t\\14t-5t^2\end{matrix}\right)$$
$$-5t^2+14t=0\rightarrow t=\frac{-14\pm\sqrt{14^2}}{-10}=2.8\ s$$
$$A=14\sqrt{3}\times2.8=67.9\ m$$
$$s_{\text{max height}}=\left(\begin{matrix}(14\sqrt{3})1.4\\14\times1.4-5t^2\end{matrix}\right)=\left(\begin{matrix}33.9\\9.8\end{matrix}\right)$$

> [!note]
> The maximum height will be half way between the two roots (of the quadratic polynomial) and half way during the flight time.
```

```ad-example
**projection from above the ground and what not**

A particle is projected from a point $O$ with speed $V\ ms^{-1}$ and at an angle of elevation $\theta$, where $\tan\theta=\frac43$. The point $O$ is $42.5\ m$ above a horizontal plane. THe particle strikes the plane at a point $A, 5\ s$ after it is projected.

Show that $V=16.5$. Find the distance between $OA$.

$$O=\left(\begin{matrix}0\\42.5\end{matrix}\right)$$
$$A=\left(\begin{matrix}x\\0\end{matrix}\right)$$
$$s=\left(\begin{matrix}x\\-42.5\end{matrix}\right)$$
$$u=\left(\begin{matrix}\frac35V\\\frac45V\end{matrix}\right)$$
$$a=\left(\begin{matrix}0.0\\-10.0\end{matrix}\right)$$
$$t=5$$
$$s=ut+\frac12at^2$$
$$\left(\begin{matrix}x\\-42.5\end{matrix}\right)=\left(\begin{matrix}\frac35V\\\frac45V\end{matrix}\right)5+\frac12\left(\begin{matrix}0.0\\-10.0\end{matrix}\right)5^2$$
$$\left(\begin{matrix}x\\-42.5\end{matrix}\right)=\left(\begin{matrix}3V\\5V-5^3\end{matrix}\right)$$
this yields
$$V=16.5\ ms^{-1}$$
$$\implies x=49.5\ m$$
$$OA=\sqrt{49.5^2+(-42.5)^2}=65.2\ m$$

> [!note]
> The maximum height will be half way between the two roots (of the quadratic polynomial) and half way during the flight time.
```

```ad-example
**time above a given point and what not**

A particle is projected a point $O$ with speed $35\ ms^{-1}$ and at angle of elevation of $30^\circ$. The particle moves freely under gravity. Find the length of time for which the particle is $15\ m$ or more above $O$.

$$O=\left(\begin{matrix}0\\0\end{matrix}\right)$$
$$s=\left(\begin{matrix}x\\15\end{matrix}\right)$$
$$u=\left(\begin{matrix}17.5\sqrt{3}\\17.5\end{matrix}\right)$$
$$a=\left(\begin{matrix}0.0\\-10.0\end{matrix}\right)$$
$$t=t$$
$$s=ut+\frac12at^2$$
$$\left(\begin{matrix}x\\15\end{matrix}\right)=\left(\begin{matrix}17.5\sqrt{3}\\17.5\end{matrix}\right)t+\frac12\left(\begin{matrix}0.0\\-10.0\end{matrix}\right)t^2$$
$$\left(\begin{matrix}x\\15\end{matrix}\right)=\left(\begin{matrix}17.5\sqrt{3}t\\17.5t-5t^2\end{matrix}\right)$$
$$t_0=1.5, t_1=2$$
$$\Delta t = 0.5\ s$$
```

```latex
$$r_0=\left(\begin{matrix}0\\0\end{matrix}\right)$$
$$u=\left(\begin{matrix}25.0\\0.0\end{matrix}\right)$$
$$v=\left(\begin{matrix}\end{matrix}\right)$$
$$a=\left(\begin{matrix}0.0\\-10.0\end{matrix}\right)$$
$$t=t$$
```

# General Case
A particle is projected from a point on a horizontal plane with an initial velocity $𝑈$ at an angle $𝛼$ above the horizontal and moves freely under gravity until it hits the plane at point $𝐵$. Given that that acceleration due to gravity is $𝑔$, find expressions for: 

the time of flight, $𝑇$ the range, $𝑅$, on the horizontal plane.

$$r_0=\left(\begin{matrix}0\\0\end{matrix}\right)$$
$$r_1=\left(\begin{matrix}B\\0\end{matrix}\right)$$
$$s=\left(\begin{matrix}B\\0\end{matrix}\right)$$
$$u=\left(\begin{matrix}U\cos\alpha\\U\sin\alpha\end{matrix}\right)$$
$$a=\left(\begin{matrix}0.0\\g\end{matrix}\right)$$
$$t=t$$
$$s=ut+\frac12at^2$$

$$\left(\begin{matrix}B\\0\end{matrix}\right)=\left(\begin{matrix}U\cos\alpha\\U\sin\alpha\end{matrix}\right)t+\frac12\left(\begin{matrix}0.0\\g\end{matrix}\right)t^2$$
$$\left(\begin{matrix}B\\0\end{matrix}\right)=\left(\begin{matrix}Ut\cos\alpha\\Ut\sin\alpha+\frac12gt^2\end{matrix}\right)$$
$$t(U\sin\alpha+\frac12gt)=0\implies U\sin\alpha+\frac12gt=0$$
this yields the time of flight, $t$:
$$t=-\frac{2U\sin\alpha}{g}$$

which yields the range of the flight, $R$:
$$R=B=-\frac{2U^2\sin\alpha\cos\alpha}{g}=-\frac{U^2\sin2\alpha}{g}$$

on the other side of the hand, the equation of the trajectory, $y$:
$$y=x\tan\alpha+\frac{gx^2}{2U^2}(1+\tan^2\alpha)$$