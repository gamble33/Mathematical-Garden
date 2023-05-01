
```ad-definition
**Angular speed** is the measure of the rate of rotation.

Units: $\text{rad}\ s^{-1}$
```

```ad-note
Angular velocity suggests a direction, either clockwise or anti-clockwise.
```

A time period, $T$, of $1\ s$ implies an angular speed of $2\pi\ \text{rad}\ s^{-1}$.

```ad-example
If an engine does $3000\ rpm$, then:
$$\omega=\frac{3000}{60}\times2\pi=100\pi\ \text{rad}\ s^{-1}\approx
314\ \text{rad}\ s^{-1}$$
```

Consider a particle moving around a circle of radius $r$. In a small instance of time, $dt$, the particle would have moved an angle of $d\theta$. This means the path of the particle will be $rd\theta$ in length.
$$ds=rd\theta$$
$$\implies \frac {ds} {dt} = \frac {rd\theta} {dt}$$
$$\implies v = r\omega$$

Consider a point, $P$, moving around the circumference of a circle with radius $r$. The position vector of $P$ will be:
$$s=\left(\begin{matrix}r\cos\theta\\r\sin\theta\end{matrix}\right)$$
let $\frac{d\theta}{dt}=\omega$ be a constant. At the time $t=0$, let $\theta=0$. 
$$\frac{d\theta}{dt}=\omega$$
$$d\theta=\omega dt$$
$$\int d\theta=\int\omega\ dt$$
$$\theta=wt+C$$
$$C=0$$
$$\implies \theta=\omega t$$

Thus, $\theta$ can be equated to $\omega t$.
Therefore,
$$s(t)=\left(\begin{matrix}r\cos{\omega t}\\r\sin{\omega t}\end{matrix}\right)$$
$$\frac{ds(t)}{dt}=v(t)=\left(\begin{matrix}-r\omega\sin{\omega t}\\r\omega\cos{\omega t}\end{matrix}\right)$$
$$\frac{dv(t)}{dt}=a(t)=\left(\begin{matrix}-r\omega^2\cos{\omega t}\\-r\omega^2\sin{\omega t}\end{matrix}\right)$$
Calculating the linear velocity and linear acceleration is as follows:
$$|v(t)|=\sqrt{r^2\omega^2(\sin^2\omega t+\cos^2\omega t)}=r\omega$$
$$|a(t)|=r\omega^2$$
```ad-note
The main tools we will be using for working out the circular motions of particles will be:
$$a=r\omega^2$$
$$v=r\omega$$
$$a=\frac{v^2}{r}$$
$$F=ma$$
$$\frac12mu^2+mgh_0=\frac12mv^2+mgh_1$$
```

# Horizontal Circle
```ad-example
A car of mass 𝑀kg is travelling round a bend which is an arc of a circle of radius 140 m. The greatest speed at which the car can travel round the bend without slipping is 45𝑘𝑚 ℎ^(−1). Find the coefficient of friction between the tyres of the car and the road.

![[Circular Motion 2023-04-05 10.49.09.excalidraw]]

$$45\ kmh^{-1}=\frac{45\times10^3}{60^2}=12.5\ ms^{-1}$$
$$R=Mg$$
$$\mu Mg=\frac{Mv^2}{r}$$
$$\mu=\frac{v^2}{rg}$$
$$\mu=\frac{12.5^2}{140\times10}=0.112$$
```

## Conical Pendula
```ad-example
A particle of mass 2 kg is attached to one end of a light inextensible string of length 0.5 m. The other end of the string is attached to a fixed point A. The particle moves with constant angular speed in a horizontal circle of radius 0.4 m. The centre of the circle is vertically below A. Calculate the tension in the string and the angular speed of the particle.

![[Circular Motion 2023-04-05 11.43.42.excalidraw]]
Resolving vertically:
$$2g=T\sin\theta$$
$$\text{height}=0.3\ m$$
$$\sin\theta=\frac{0.3}{0.5}$$
$$\cos\theta=\frac{0.4}{0.5}$$
$$T=\frac{2g}{\frac{0.3}{0.5}}=\frac{100}{3}\ N$$
resolving horizontally,
$$a=r\omega^2$$
$$\frac12T\cos\theta=0.4\omega^2$$
$$\omega=\sqrt{\frac{\frac{100}{6}\times\frac45}{\frac25}}=5.77
\ \text{rad}\ s^{-1}$$
```

## Two Strings Problem
```ad-example
A particle P of mass 𝑚 is attached by two strings to fixed points A and B, where A is vertically above B. The strings are both taught and P is moving in a horizontal circle with constant angular speed 2√3𝑔 𝑟𝑎𝑑 𝑠^(−1).Both strings are 0.5m in length and inclined at 60° to the vertical. Calculate the tension in the two strings.

![[Circular Motion 2023-04-05 12.29.14.excalidraw]]

$$\omega=2\sqrt{3g}\ \text{rad}\ s^{-1}$$
resolving vertically:
$$T_A \cos 60=mg+T_B\cos60$$
resolving horizontally:
$$T_A\sin60+T_B\sin60=r\omega^2m$$
$$T_A\sin60+T_B\sin60=6gm\sin60$$
$$T_A+T_B=6mg$$
$$T_A\cos60+T_B\cos60=6mg\cos60$$
now we have simultaneous equations:

$$T_A\cos60+T_B\cos60=6mg\cos60$$
$$T_A \cos 60-T_B\cos60=mg$$
which is equivalent to
$$T_A+T_B=6mg$$
$$T_A -T_B=2mg$$
$$2T_A=8mg$$
$$T_A=4mg$$
$$T_B=2mg$$

```

## Banked Surface
```ad-example
A boy rides his cycle round a circular track of radius 25 m. The track is banked at 20⁰ to the horizontal. There is no force due to friction. By modelling the boy and his cycle as a particle of mass 75 kg, find the speed at which the boy is cycling.

![[Circular Motion 2023-04-05 12.02.17.excalidraw]]

- [x] for an inclined planed, resolve vertically and horizontally as oppose to tangentially and normally.

Resolving vertically,
$$R\cos 20=750$$
$$\implies R = \frac{750}{\cos 20}$$
resolving horizontally,
$$R\sin20=\frac{mv^2}{r}$$
$$750\tan20=\frac{mv^2}{r}$$
$$v=\sqrt{250\tan20}=9.54\ ms^{-1}$$
```

# Vertical Circle
![[Pasted image 20230406101850.png]]
In the case of a vertical circle, a body force is present. 
```ad-definition
A **body force** is an external force that affects the entire system.

Common examples:
- magnetism
- gravity
```
In this case, the body force is gravity. Consequently, $\omega$ can no longer be assumed as constant.

The position vector of particle $P$ at time $t$ is given by:
$$s_t=\left(\begin{matrix}r\cos\theta_t\\r\sin\theta_t\end{matrix}\right)$$
$$\frac{d s_t}{dt}=v_t=\left(\begin{matrix}
-r\theta_t'\sin\theta_t \\
r\theta_t'\cos\theta_t
\end{matrix}\right)$$
The dot product of $s_t$ and $v_t$ is zero. This implies that the velocity vector $v_t$ is perpendicular to $s_t$. Thus, the velocity vector is tangential to the circle.
$$\frac{d v_t}{dt}=a_t=r\left(\begin{matrix}
-\theta_t''\sin\theta_t-\theta_t'^2\cos\theta_t \\
\theta_t''\cos\theta_t-\theta_t'^2\sin\theta_t
\end{matrix}\right)$$
$$a_t=
\overbrace{
r\theta_t''
\left(\begin{matrix}
-\sin\theta_t \\
\cos\theta_t
\end{matrix}\right)
}^{\text{tangential component}}
\underbrace{
-
r\theta_t'^2
\left(\begin{matrix}
\cos\theta_t \\
\sin\theta_t
\end{matrix}\right)
}_{\text{radial component}}
$$

Consider the radial component of acceleration 
$$a_r=-r\theta_t'^2
\left(\begin{matrix}
\cos\theta_t \\
\sin\theta_t
\end{matrix}\right)
$$
$$\implies|a_r|=r\theta_t'^2$$
$$|v_t|=r\theta_t'$$
$$|a_r|=\frac{|v_t|^2}{r}$$

```ad-example
A particle of mass 0.4kg is attached to one end of a light inextensible string of length 0.3m. The other end of the string is attached to a fixed point B. The particle is hanging in equilibrium when it is set in motion with a horizontal speed of 𝑢 ms^(−1). Find an expression for the tension in the string, in terms of 𝑢, when it is at an angle 𝜃 to the downward vertical through B.

![[Circular Motion 2023-04-06 10.50.49.excalidraw]]
Using the work energy principle,
$$0.2u^2=0.2v^2+4h_1$$
$$u^2-20h_1=v^2$$
resolving radially:
$$|a|=\frac{|v|^2}{r}$$
$$\therefore |a|=\frac{u^2-20\times0.3(1-\cos\theta)}{0.3}$$
$$F=0.4\frac{u^2-20\times0.3(1-\cos\theta)}{0.3}$$
$$T-\cos\theta\times0.4g=0.4\frac{u^2-20\times0.3(1-\cos\theta)}{0.3}$$
$$T=0.4\frac{u^2-20\times0.3(1-\cos\theta)}{0.3}+\cos\theta\times0.4g$$
```

```ad-warning
Strings vs Rods
- String can be slack if $T \leq 0$, $r$ is not preserved (a.k.a. it ceases to be circular motion). Rods can't be slack (it is constrained to circular motion).
- A circular arc past $90^\circ$ may cause a string to become slack because the radial component of weight now acts towards the centre of the circle. 
	- Therefore, in the case of a string: velocity must be great enough to provide a centripetal force which is considerabely high. If the centripetal force is greater than weight, then there must be an aditional force pulling it in (this force will be tension for rods and strings).
	- In the case of a rod, the velocity can be lower causing a centripetal force which is less than weight, therefore, the tension force in the rod must be negative (a.k.a. the rod is being compressed rather than being extended).
- If a circular motion ceases to be constrained (if the string breaks or is cut), then the particle will leave the circular motion and fall freely under gravity (projectile motion)
```

```ad-example
A particle of mass 0.4kg is attached to one end of a light inextensible string of length 0.3m. The other end of the string is attached to a fixed point B. The particle is hanging in equilibrium when it is set in motion with a horizontal speed of 𝑢 ms^(−1). 

![[Circular Motion 2023-04-06 10.50.49.excalidraw]]

(a) Find an expression for the tension in the string, in terms of 𝑢, when it is at an angle 𝜃 to the downward vertical through B.

$$T=0.4\frac{u^2-20\times0.3(1-\cos\theta)}{0.3}+\cos\theta\times0.4g$$

(b) Find the minimum value of 𝑢 for which the particle will perform a complete circle.

$$T \gt 0$$

$$0.4\frac{u^2-20\times0.3(1-\cos\theta)}{0.3}+\cos\theta\times0.4g\gt0$$
$$u^2-20\times0.3(1-\cos\theta)+0.3\cos\theta\times g\gt0$$
$$u^2\gt20\times0.3(1-\cos\theta)-0.3\cos\theta\times g$$
The angle of $\theta$ at which the string is most likely to go slack is when $\theta=\pi$.
$$u^2\gt20\times0.3(1-(-1))-0.3(-1)\times g$$
$$u^2\gt12+0.3g$$
$$u^2\gt15$$
$$u\gt3.87\ ms^{-1}$$

```

```ad-example
A particle of mass 0.4kg is attached to one end of a light ~~inextensible string~~ rod of length 0.3m. The other end of the ~~string~~ rod is attached to a fixed point B. The particle is hanging in equilibrium when it is set in motion with a horizontal speed of 𝑢 ms^(−1). 

![[Circular Motion 2023-04-06 10.50.49.excalidraw]]

(a) Find an expression for the tension in the ~~string~~ rod, in terms of 𝑢, when it is at an angle 𝜃 to the downward vertical through B.

$$T=0.4\frac{u^2-20\times0.3(1-\cos\theta)}{0.3}+\cos\theta\times0.4g$$

(b) Find the minimum value of 𝑢 for which the particle will perform a complete circle.

$$T \gt -W_\text{radial}$$

#todo FIX THIS ITS WRONG
$$0.4\frac{u^2-20\times0.3(1-\cos\theta)}{0.3}+\cos\theta\times0.4g\gt-mg\cos\theta$$
$$0.4\frac{u^2-20\times0.3(1-\cos\pi)}{0.3}+\cos\pi\times0.4g\gt-mg\cos\pi$$
$$0.4\frac{u^2-12}{0.3}-0.4g\gt mg$$
$$u^2\gt 0.6g+12$$
$$u^2\gt 18$$
$$u\gt4.24$$

```