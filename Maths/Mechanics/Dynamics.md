The study of motion with relation to the forces involved.

In this study, situations where force and/or mass is not constant will be scrutinised.

```ad-warning
So far, only situations in the context of constant acceleration have been considered. This will no longer be the case if force or mass are allowed to vary.

$sv_0v_1at$ equations will no longer apply.
```

We have already dealt with situations where acceleration is variable, usually given as a polynomial function of time.

In order to deal with these problems, calculus can be applied. Namely:

$$a=\frac {dv} {dt},\qquad v= \frac {dx} {dt}$$

As we move into dynamics, we need to consider why the acceleration may change as oppose to just considering what the acceleration function is. Thus, we consider a variable force.

Force Depending upon Time
---
- Power output of a solar panel powered by sun. Light intensity varies with respect to time.
- A car driving along, burning fuel, becoming lighter.
- A runner getting tired, putting less effort into their legs.
- A jet engine coming up to full speed.

Force Depending upon Displacement
---
As spaceship leaves and increases its displacement from earth, the force of gravity, incident upon the spaceship, decreases 
$$F=G\frac{m_1m_2}{r^2}$$

A sprung suspension being compressed.

Force Depending upon Velocity
---
A skydiver who unleashes her parachute will create a drag force which will be greater at a higher velocity.

An oil filled suspension being compressed.

# Calculations
The general strategy is to take the formula $F=ma$ and rearrange to make $a$ the subject. 

Notice that $F$ and therefore $a$ must be a function of time, displacement of velocity. Therefore, we will have two primary equations for $a$.

**If force is a function of time** (or if force is a function of velocity where time is a relevant factor)
---

$$\frac{F}{m}=\frac{dv}{dt}=\frac{d^2x}{dt^2}$$

```ad-example
$$F(t)=3t^2-t$$
Find $v(t)$ given that $v(0)=2$ and $m=1$.
$$\frac{dv}{dt}=\frac{3t^2-t}{1}$$
$$\implies \int dv = \int (3t^2-t)\ dt$$
$$v(t)=t^3-\frac12t^2+C$$
$$C=2$$
$$v(t)=t^3-\frac12t^2+2$$
Find $x(t)$ given that $x(0)=0$.
$$\int v(t)\ dt=x(t)$$
$$\implies x(t)=\frac14t^4-\frac16t^3+2t$$
```

**If force is a function of displacement** (or if force is a function of velocity where displacement is a relevant factor)
---

$$a=\frac{dv}{dt}=\frac{dv}{dx}\times\frac{dx}{dt}=\frac{dv}{dx}\times v$$

$$\frac{F}{m}\stackrel{\_}{\_}v\frac{dv}{dx}$$

$$\frac{F}{m}=\frac{d}{dx}\left(\frac12v^2\right)$$

```ad-example
$$F(x)=3x^2-x$$
Find $v(x)$ given that $v(0)=2$ and $m=1$.
$$v\frac{dv}{dx}=\frac{3x^2-x}{1}$$
$$\implies \int v\ dv = \int (3x^2-x)\ dx$$
$$\frac12(v(x))^2=x^3-\frac12x^2+C$$
$$C=2$$
$$v(x)=x^3-\frac12x^2+2$$
```

Some Useful Integrals
---
$$\int F(t)\ dt = \text{impulse (total change in momentum)}$$

$$\int F(x)\ dx = \text{work done}$$


Examples of the Above
---

```ad-example
A pebble of mass 0.2kg is moving on a smooth horizontal sheet of ice. At time 𝑡 seconds (where 𝑡≥0) a horizontal force of magnitude 2𝑡^2 N and constant direction acts on the pebble. When 𝑡=0 the pebble is moving in the same direction as the force and has a speed of 6𝑚𝑠^(−1). When 𝑡=𝑇 the pebble has a speed of 36𝑚𝑠^(−1). Calculate the value of 𝑇.

$$v(0)=6\ ms^{-1}, \qquad v(T)=36\ ms^{-1}$$
Given that $F(t)=m\times a(t)$:
$$2t^2=0.2 \times a(t) \implies a(t)=10t^2$$
Given that $a(t)=\frac{dv}{dt}$:
$$dv=10t^2\ dt$$
$$\implies \int dv=\int 10t^2\ dt$$
$$\implies v(t)=\frac{10}{3}t^3 + C$$
Given that $v(0)=6\ ms^{-1}$, $C$ must be equal to $6$
$$v(t)=\frac {10} {3} t^3 + 6$$
$$36=\frac{10}{3}T^3+6$$
$$90=10T^3$$
$$9=T^3 \implies T = \sqrt[3]{9}$$
```

```ad-example
A particle $P$ of mass $1.5\ kg$ is moving in a straight line. The force acting on P has magnitude $(8−2\cos 𝑥)\ 𝑁$, where $𝑥$ meters is the distance $OP$, and acts in the direction $OP$. When $P$ passes through $O$ its speed is $4\ 𝑚𝑠^{−1}$. Calculate the speed of $P$ when $𝑥=2$.

$$F(x)=8-2\cos x$$
$$\frac{8-2\cos x}{1.5}=v\frac{dv}{dx}$$
$$\frac23\int8-2\cos x\ dx=\int v\ dv$$
$$\frac{16}3x-\frac43\sin x=\frac12v^2+C$$
$$v^2=\frac{32}3x-\frac83\sin x+16$$
$$v(x)=\sqrt{\frac{32}3x-\frac83\sin x+16}$$
$$v(2)=\sqrt{\frac{32}3\times2-\frac83\sin 2+16}$$
$$v(2)\approx5.91\ ms^{-1}$$
```

Examples of Force as a Function of Velocity
---

```ad-example
a particle of mass $0.5kg$ moves in a straight horizontal line. When the speed of $P$ is $\nu\ 𝑚𝑠^{−1}$, the resultant force acting on $P$ is a resistance of magnitude $3\nu\ N$. Find the distance moved by $P$ as it slows down from $12𝑚𝑠^{−1}$ to $6𝑚𝑠^{−1}$.

$$m=0.5\ kg$$
$$v(\nu): \sum F=-3\nu$$

$$\frac{F}{m}=-6v=v\frac{dv}{dx}$$
$$-6=\frac{dv}{dx}$$
$$-6x=v+C$$
$$v=-6x-C$$
$$v(x_1)=12,\qquad v(x_2)=6$$
$$\implies \begin{matrix}-6x_1-C=12\\-6x_2-C=6\end{matrix}$$
$$-6x_1+6x_2=6$$
$$-6(x_1-x_2)=6$$
$$x_2-x_1=1\ m$$
```

```ad-example
A car of mass 800kg travels along a straight horizontal road. The engine of the car produces a constant driving force of magnitude 2000N. At time 𝑡 seconds, the speed of the car is 𝑣𝑚𝑠^(−1). As the car moves, the total resistance to motion of the car is magnitude (400+4𝑣^2)N. The car starts from rest.Find 𝑣 in terms of 𝑡 and, hence, show that the car cannot exceed 20𝑚𝑠^(−1).

$$\frac{2000-(400+4v^2)}{800}=\frac{dv}{dt}$$
$$1600-4v^2=800 \frac{dv}{dt}$$
$$\int dt=\int\frac{800}{1600-4v^2} \ dv$$
$$\int dt=200\int\frac{1}{400-v^2} \ dv$$
$400-v^2=(20+v)(20-v)$
$$\implies \int dt=200\int\frac{1}{(20+v)(20-v)} \ dv$$
$$\int dt = 5\int\frac{1}{20-v}+\frac{1}{20+v}\ dv$$
$$t=5(\ln (20+v)-\ln(20-v))+C$$
$$C=0$$
$$t=5(\ln (20+v)-\ln(20-v))$$
$$\frac{20+v}{20-v}=e^{\frac15 t}$$
$$v=\frac{20(e^{\frac15t}-1)}{e^{\frac15t}+1}$$
$$\frac{e^{\frac15t}-1}{e^{\frac15t}+1}\lt1$$
```

# Applications
Google
YouTube
Instagram

## Gravitation
The law of gravitational force is
$$F=G\frac{m_1m_2}{r^2}$$
where:
- $F$ is the gravitational force ($N$)
- $G$ is the gravitational constant $\approx6.67\times10^{-11}\ \frac{m^3}{s^2kg}$
- $m_1$ mass of the first body ($kg$) 
- $m_2$ mass of the second body ($kg$) 
- $r$ the distance between the centres of the bodies ($m$)

Generally speaking, it is easier to use the formula:
$$F=\frac{k}{d^2}$$
where:
- $F$ is the gravitational force ($N$)
- $k$ is a constant ($Nm^2$).
- $d$ is distance ($m$)

```ad-example
Above the Earth’s surface, the magnitude of the force on a particle due to the Earth’s gravitational force is inversely proportional to the square of the distance of the particle from the centre of the Earth. The acceleration due to gravity on the surface of the Earth is 𝑔 and the Earth can be modelled as a sphere of radius 𝑅. A Particle P of mass 𝑚 is a distance (𝑥−𝑅), (where 𝑥≥𝑅), above the surface. 

Prove that the magnitude of the gravitational force acting on 𝑃 is $\frac{𝑚𝑔𝑅^2}{𝑥^2}$

$$F=\frac{k}{d^2}$$
$$mg=\frac{k}{R^2}$$
$$k=mgR^2$$
From a distance $(x-R)$ above the Earth's surface, $d=R+(x-R)=x$ as $d$ is measured from the centre (rather than the surface) of the Earth.
$$F=\frac{k}{x^2}$$
$$\implies F=\frac{mgR^2}{x^2}$$

A spacecraft, is fired vertically upwards from the surface of the Earth. When it is at a height 2𝑅 above the surface of the Earth its speed is $\frac12 \sqrt{𝑔𝑅}$. Assuming that air resistance can be ignored and that the rocket’s engine is turned off immediately after the rocket is fired, Find, in terms of 𝑔 and 𝑅, the speed with which 𝑆 was fired.

$$-\frac{gR^2}{x^2}=v\frac{dv}{dx}$$
$$-\frac{gR^2}{x^2}dx=v\times dv$$
$$-gR^2\int\frac{1}{x^2}\ dx=\int v\ dv$$
$$\frac{gR^2}{x}=\frac12v^2+C$$
$$\frac{gR^2}{3R}=\frac18gR+C$$
$$\frac{5}{24}gR=C$$
$$\frac{gR^2}{x}=\frac12v^2+\frac{5}{24}gR$$
now we substitute $x=R$ and solve for $v$.
$$2gR=v^2+\frac{5}{12}gR$$
$$\frac{19}{12}gR=v^2$$
$$v=\sqrt{\frac{19}{12}gR}$$
```

## Simple Harmonic Motion
Simple harmonic motion is motion in which the acceleration of a particle is always directed towards a fixed point. The **acceleration is proportional to the displacement** of the particle from the fixed point.

$$F=-kx$$
where:
- $F$ is the restorative force ($N$)
- $k$ is the constant of proportionality.
- $x$ is the displacement from the fixed point $m$.

Rewriting in terms of acceleration:
$$a=-\omega^2 x$$

A particle $P$ moves with simple harmonic motion about a point $O$. Given that the maximum displacement of the particle from $O$ is $A$ (amplitude), the following results can be found.

$$a=-\omega^2x$$
$$\frac{dv}{dt}=v\frac{dv}{dx}=-\omega^2x$$
$$\int v\ dv=-\omega^2\int x\ dx$$
$$\frac12v^2=-\frac12\omega^2x^2+C_0$$
$$v^2=-\omega^2x^2+C_1$$
$v|_{x_{\text{max}}}=0$
$$\implies 0=-\omega^2A^2+C_1$$
$$C_1=\omega^2A^2$$
$$\therefore v=\omega\sqrt{A^2-x^2}$$
$$ $$
$$\frac{dx}{dt}=\omega\sqrt{A^2-x^2}$$
$$(A^2-x^2)^{-\frac12}\ dx=\omega\ dt$$
$$\int(A^2-x^2)^{-\frac12}\ dx=\int\omega\ dt$$
$$\arcsin \left(\frac{x}{A}\right)=\omega t+C_2$$
$$x=A\sin(\omega t+C_2)$$
$$\color{aquamarine} x=A\sin(\omega t+\alpha)$$

![[Pasted image 20230426130907.png]]
$$a=0 \implies \arcsin \omega t$$
$\implies$ we start at the equilibrium position. "Particle given initial velocity."

![[Pasted image 20230426130956.png]]
$$a=\frac \pi 2 $$

![[Pasted image 20230426131048.png]]

```ad-summary
For SHM of amplitude $A$, we have: 
$$a=-\omega^2x$$
$$v^2=\omega^2{(A^2-x^2)}$$
$$x=A\sin(\omega t + \alpha)$$
The period of oscillation would be $T=\frac{2\pi}{\omega}$
```

```ad-example
A particle 𝑃 of mass 0.8kg is attached to the ends of two identical light elastic strings of natural length 1.6m and modulus of elasticity 16N. The free ends of the strings are attached to two points A and B which are 4m apart on a smooth horizontal surface. The point C lies between A and B such that ABC is a straight line and AC=2.4m. The particle is held at C and is then released from rest. 

![[Dynamics 2023-04-27 10.52.50.excalidraw]]

Show that the subsequent motion is simple harmonic motion.

When $x=x$
$$T_A=-\frac{16}{1.6}\times(0.4+x)$$
$$T_B=\frac{16}{1.6}\times(0.4-x)$$

$$\sum F=ma=-\frac{32}{1.6}x$$
$$a=-\frac{32}{1.6\times0.8}x$$
$$a=-25x \implies \omega=5$$
Acceleration is negative and proportional to, and only to, displacement therefore the system exhibits qualities of simple harmonic motion.

Find the period and amplitude of the motion.

When $x=0.4$
$$T_A=-\frac{16}{1.6}\times0.8$$
$$T_B=\frac{16}{1.6}\times0$$

$$A=0.4\ m$$
$$T=\frac{2\pi}{5}=1.26\ s$$

Calculate the maximum speed of P.

$$v_{\text{max}}=\omega A=5\times0.4=2\ ms^{-1}$$
```

```ad-warning
The centre of oscillation for simple harmonic motion is the point of equilibrium.
- for a single spring/pendulum this will be the natural length/$\theta=0$.
- for a paired-spring system, the equilibrium will need to be calculated.
- for a vertical system, the weight will impact the equilibrium position.
```