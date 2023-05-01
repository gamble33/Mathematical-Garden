# Introduction

$$P=mv$$
where:
- $P$ is momentum ($kgms^{-1}$ or $Ns$)
- $m$ is mass ($kg$)
- $v$ is velocity ($ms^{-1}$)

```ad-note
Note that velocity is a vector as is force, therefore, momentum will also be a vector.
```

If we differentiate $P$ with respect to time, we find force.
$$F=\frac{dP}{dt}$$

$$F\times dt=dP$$
$$\int^{t_1}_{t_0} F\times dt=\int^{t_1}_{t_0} dP$$
$$\left[F(t)\times t\right]^{t_1}_{t_0}=I=\text{impulse}$$
The impulse is the difference between the momentum initially and the final momentum. Impulse is, thus, also measured in $Ns$

```ad-observation
When modelling a collision, we generally consider the change to be instantaneous. In reality, this is never the case.

In order to change the momentum of an object, a force must be applied over a period of time. Therefore, there must be contact between the two objects for that time period.

Consider a ball hitting a bat. It appears as though this interaction is instantenous, however, if you view the interaction in slow-motion, you will see the ball making contact; the bat bending; the ball compressing, and then those same processes in reverse. This will all take a fraction of a second but some time (it is not instantenous).
```

# Collisions

**Newton's Third Law**
Newton states that for every action in nature, there is an equal and opposite reaction.

So far in our study, we've interpreted action to mean force. However, in the study of momentum, the action can be impulse.

Therefore, if two particles collide ($A$ and $B$) the impulse that $B$ exerts on $A$ will be equal and opposite to the impulse that $A$ exerts on $B$.

The result to this equal and opposite impulse is that on the given system, the total impulses will cancel out. Therefore, we arrive at the law of **conservation of momentum**.

$$\sum P_i = \sum P_f$$

```ad-example
**Missing Mass**

Two particles $A$ and $B$, of mass $0.3\ kg$ and $m\ kg$ respectively, are moving in opposite directions along the same straight horizontal line so that the particles collide directly. Immediately before the collision, the speeds of $A$ and $B$ are $8\ ms^{-1}$ and $4\ ms^{-1}$. respectively. In the collision the direction of motion of each particle is reversed and, immediately after the collsiion, the speed of each particle is $2\ ms^{-1}$.

Find the magnitude of the impulse exerted by $B$ on $A$ in the collsiion.

$$I=-2\times0.3 - 8\times 0.3=-3\ Ns$$

Find the mass of particle $B$.

$$8\times0.3-4m=-2\times0.3+2m$$
$$0.3(8+2)=6m \implies m=0.5\ kg$$
```

```ad-example
**Missing Velocity**

Consider two particles $A$ and $B$ with masses and $2\ kg$ and $1\ kg$ respectively moving in the same direction where $A$ has a velocity of $3\ ms^{-1}$ and $B$ has a velocity of $1\ ms^{-1}$. Following a collsion $A$ now has a velocity of $1\ ms^{-1}$.

![[Pasted image 20230427121034.png]]

Find the velocity of $B$

$B$ exerts an impulse on $A$ of:
$$I=1\times2-3\times2=-4\ Ns$$
Therefore, $A$ must exert an impulse of $4\ Ns$ on $B$.
$$I_B=4=v_2-1$$
$$\implies v_2=5\ ms^{-1}$$
```

Combining Particles
---
When two particles combine, their velocities will be equal. They can be treated as one particle with a mass equal to the sum of the masses of its constituents. 

We see this in examples such as particles connected by string or trains linking together.

```ad-example
Two particles P and Q, of masses 8kg and 2kg respectively, are connected by a light inextensible string. The particles are at rest on a smooth horizontal plane with the string slack. Particle P is projected directly away from Q with speed $4\ 𝑚𝑠^{−1}$. Find the common speed of the particles after the string goes taut. Find the magnitude of the impulse transmitted through the string when it goes taught.

![[Momentum & Impulse 2023-04-27 12.30.34.excalidraw]]

$$8\times4+2\times0=8v+2v$$
$$32=10v \implies v = 3.2\ ms^{-1}$$

$$I_Q=2(v-0)=2v=6.4\ Ns$$
```

```ad-example
A truck $P$ of mass $2M$ is moving with speed $U$ on smooth straight horizontal rails. It collides directly with another truck $Q$ of mass $3M$ which is moving with speed $4U$ in the opposite direction on the same rails. The trucsk join so that immediately after the collsion they move together. By modelling the trucks as particles,

![[Momentum & Impulse 2023-04-27 12.39.15.excalidraw]]

find the speed of the trucks immediately after the collision.

$$2MU-12MU=5Mv$$
$$-10U=5v$$
$$v=-2U$$
$$|v|=2U$$

Find the magnitude of the impulse exerted on $P$ by $Q$ in the collision.

$$I_P=2M(v-U)=-6MU$$
$$|I_P|=6MU$$
```

# Inelastic Collisions
So far we have considered collisions where there is one unknown value ($v$ or $m$). However, we can also consider systems where both final velocities are unknown. Notice, this introduces a second unknown and therefore will require a simultaneous equation.

One of the equations in the system will be the conservation of momentum.

The second equation will be the loss of relative kinetic energy which is calculated by the material property known as the coefficient of restitution.

The coefficient of restitution, $e$, has no units (similar to friction). It is a value between $0$ and $1$ (similar to friction). It measures the relative velocity before and after a collision.

If $e=1$, we describe the collision as perfectly elastic.

If $e=0$, the collision is totally inelastic. In other words, the particles will coalesce/join together.

$$e=\frac{v_1-v_0}{u_0-u_1}$$

As such, $e$ can be thought of as the percentage of relative velocity conserved.

```ad-example
Two particles A and B of masses 200g and 400g respectively are travelling in opposite directions towards each other on a smooth surface with speeds of 5𝑚𝑠^(−1) and 4𝑚𝑠^(−1) respectively. They collide directly, and immediately after their collision have velocities 𝑣_1 𝑚𝑠^(−1) and 𝑣_2 𝑚𝑠^(−1) respectively, measured in the direction of the motion of A before the collision. Given that the coefficient of restitution between A and B is 1/2, find 𝑣_1and 𝑣_2

![[Momentum & Impulse 2023-04-27 13.05.40.excalidraw]]

**Newton's Law of Restitution**
$$e=\frac{v-u}{5-(-4)}=\frac{v-u}{9}=\frac12$$
$$\implies v-u=4.5$$

**Conservation of Momentum**
$$1-1.6=0.2u+0.4v$$
$$-6=2u+4v$$

Solving Simultaneously
$$-3=u+2(4.5+u)$$
$$-3=9+3u$$
$$u=-4\ ms^{-1}$$
$$\implies v =0.5\ ms^{-1}$$
```

## Finding Limiting Values of Problems
Problem solving questions can ask us to find limits/maxima of velocities. 

Some questions to ask our selves to help:
- Directions of particles?
- Limits of $e \in [0,1]$?
- Collision Logic (big particle wins)?
- Future collisions?

```ad-example
![[Pasted image 20230501145028.png]]
Using conservation of momentum:
$$-2=-2v_1-3v_2$$
$$2=2v_1+3v_2$$
$$e=\frac{v_1-v_2}{u_0-u_1}=\frac{v_1-v_2}{9}$$
$$=\frac{\frac{2-3v_2}{2}-v_2}{9}$$
$$e=\frac{2-5v_2}{18}$$
$$\implies 0\leq \frac{2-5v_2}{18} \leq 1$$

$$-\frac{16}{5} \leq v_2 \leq \frac52$$
Direction of $v_2$ is unchanged, therefore:
$$0 \lt v_2 \leq \frac52$$
```

```ad-example
![[Pasted image 20230501151933.png]]
$$0 \leq e \leq 1$$
by conservation of momentum,
$$10u-12u=-2ku-3v_2$$
$$-2u=-2ku-3v_2$$
$$2u(1-k)=3v_2$$
by coefficient of restitution:
$$e=\frac{ku-v_2}{9u}$$
$$e=\frac{ku-v_2}{9u}$$
$$e=\frac{3ku-2u(1-k)}{27u}$$
$$e=\frac{5k-2}{27}$$
$$\implies 0 \leq \frac{5k-2}{27} \leq 1$$
$$\frac25 \leq k \leq \frac {29} {5}$$
this is the result of using the coefficient of restitution as a limit. However, if the maximum impulse of the particles is taken into account:
$$I_{\text{max}}=4u\times3-0\times3=12u$$
$$P_{\text{max}}=5u\times2-12u=-2u$$
thus,
$$v_{\text{max}}=-u$$
This implies $k$ has an upper bound of $1$.
$$\frac25 \leq k \leq 1$$
```


```ad-example
![[Pasted image 20230501154131.png]]
The $3\ kg$ particle must be able to catch up to the $2\ kg$ particle in order for a collision to occur.
$$u_2\gt2$$
$v_2$ must be less than $4$. If $v_2$ was greater than $4$, then the collision wasn't completed.
$$v_2\leq4$$
$$0 \leq e \ \leq 1$$
$$e=\frac{4-v_2}{}$$
```

```ad-example
Two balls P and Q have masses 3𝑚 and 4𝑚 respectively. They are travelling in opposite directions towards each other along the same straight line on a smooth level floor. Immediately before they collide, P has a speed 3𝑢 and Q has a speed 2𝑢. The coefficient of restitution between P and Q is 𝑒. Given that the direction of motion of P is unchanged, find the range of possible values of 𝑒 (You may model the balls as smooth spheres).

![[Momentum & Impulse 2023-05-01 16.08.25.excalidraw]]
$$9mu-8mu=3mv_P+4mv_Q$$
$$u=3v_P+4v_Q$$
$$e=\frac{v_Q-v_P}{3u-(-2u)}=\frac{v_Q-v_P}{5u}$$
$$5eu=v_Q-v_P$$
$$20eu=u-3v_P-4v_P$$
$$u(20e-1)=-7v_P$$
$$u(1-20e)=7v_P$$
$$e=\frac1{20}-\frac {7v_P}{20u}$$
$$e=\frac{\frac{7v_Q}{u}-1}{15}$$
$$v_P \gt 0 \implies 0 \leq e \leq \frac 1 {20}$$
```

# Hitting a Wall
The collision with a wall is treated the same way it is treated between two particles with the exception that the second particle is considered to be stationary before and after the collision.

Consequently, the new formation of $e$ becomes,
$$e=\frac{\text{speed of rebound}}{\text{speed of approach}}$$
```ad-warning
When colliding with a smooth wall, impulse can only be delivered perpendicular to the wall.
```

```ad-note
You might also have to use $sv_0v_1at$ equations to find the speed immediately before impact - particularly with particles moving in a vertical line.
```

**Problem Solving Example**

A ball is dropped from a height $h\ m$. The coefficient of restitution between the wall and the ground is $e$. What is the total distance travelled by the ball before it comes to rest permanently.

$s=-h$
$u=0$
$v=v$
$a=-10$
$t=t$

$$v^2=u^2+2as$$
$$v=\sqrt{20h}$$

$$e=\frac{v_1}{\sqrt{20h}}$$
$$v_1=e\sqrt{20h}$$
$s=h_1$
$u=e\sqrt{20h}$
$v=0$
$a=-10$
$t=t$
$$h_1=-\frac{u^2}{2a}$$
$$h_1=-\frac{e^220h}{-20}$$
$$h_1=e^2h$$
$$e=\frac{v_2}{e\sqrt{20h}}$$
$$v_2=e^2\sqrt{20h}$$
$s=h_2$
$u=e^2\sqrt{20h}$
$v=0$
$a=-10$
$t=$
$$v^2=u^2+2as$$
$$s=\frac{e^420h}{20}=e^4h$$
The maximum height reached after each bounce follows the geometric sequence 
$$H_n=(e^2\times h)[e^{2}]^{n-1}$$
$$\implies \sum^\infty_{r=1}(e^2\times h)[e^{2}]^{r-1}=\frac{he^2}{1-e^2}$$
$$\implies \text{total displacement from bounces}=\frac{2h}{1-e^2}$$
$$\text{total displacement} = \frac{2h}{1-e^2}+h$$