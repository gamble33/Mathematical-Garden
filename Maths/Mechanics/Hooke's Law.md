# Introduction

$$T=-\frac\lambda l x$$
where:
- $T$ is the tension (force) ($N$)
- $l$ is the natural length of the spring/string/wire ($m$)
- $x$ is the extension ($m$)
	- $\therefore \frac x l$ can be thought of as the percentage increase/decrease (unit-less).
- $\lambda$ is the modulus of elasticity. It can be thought of as the force needed to double the length ($N$).

```ad-warning
The modulus of elasticity, $\lambda$, is not the same as Young's Modulus.

Young's Modulus is the pressure needed to double the length of a string/wire.

Therefore, if Young's Modulus is multiplied by the cross-sectional area, the modulus of elasticity would be calculated.
```

The modulus of elasticity, $\lambda$, is a fixed property of a material.

If we extend a string too far, it will deform plastically (permanent distortion) and no longer return to its original length. This will change the $\lambda$ quantity of that material.

Every item has a limit at which it no longer deform elastically. This is called the **elastic limit**. After the elastic limit, either, plastic deformation or a fracture occurs.

Likewise, not every material will extend linearly. However, in a short interval every material can be approximated to a linear extension. This is called the limit of proportionality.

```ad-tip
All questions in A-level Further Maths will be restricted to:
- linearly elastic models. In other words, they obey Hooke's Law.
- Light strings which do not extend under their own weight.
```

```ad-tip
Difference between a *string* and a *spring*.

A string will stretch the same as a spring.

A spring will have an associated compressive force under a compression, whereas, a string will just become slack.
```

# Calculations

```ad-example
An elastic string of natural length $2\ m$ and modulus of elasticity $29.4\ N$ has one fixed end. A particle of mass $4\ kg$ is attached to the other end and hangs at rest. Find the extension of the string.

$l=2\ m$
$\lambda = 29.4\ N$
$m=4\ kg$

![[Pasted image 20230424114355.png]]

$$T=mg=40\ N$$

$$T=-\frac \lambda l x$$
$$40=-\frac \lambda l x$$
$$x=\frac{Tl}{\lambda}$$
$$x=\frac{40\times 2}{29.4}=2.72\ m$$
```

# Paired Strings/Springs
Setup a pair of simultaneous Hooke's Law equations and solve simultaneously.

```ad-note
$$x_1+x_2=l_1+l_2-\text{length}$$
```

```ad-tip
All paired strings and springs will be collinear.
```

```ad-warning
Check the wording of the question carefully to check whether the weight of the mass will affect the system.
```

```ad-example
The elastic springs PQ and QR are joined together at Q to form one long spring. The spring PQ has natural length 1.6m and modulus of elasticity 20N. The spring QR has natural length 1.4m and modulus of elasticity 28N. The ends P and R, of the long string are attached to two fixed points which are 4m apart on the same horizontal plane. [Assume Q is at rest and in equilibrium]. Find the Tension in the combined spring.

![[Hooke's Law 2023-04-24 12.00.18.excalidraw]]

$$T_1=\frac{20}{1.6}x$$
$$T_2=\frac{28}{1.4}(1-x)$$

As the system is at rest, $T_1=T_2$.
$$\implies \frac{20}{1.6}x=\frac{28}{1.4}(1-x)$$
$$\frac{20}{1.6}x=\frac{28}{1.4}(1-x)$$
$$x=\frac{8}{13}=0.615\ m$$
$$T=\frac{20}{1.6}\times0.615=\frac{100}{13}\approx7.69\ N$$
```

# Energy
Energy is a measure of work that has been done in a system. Stored/potential energy is a measure of work that can be done to a system.

In the context of kinematics, work done is a measure of the force that is being acted against evaluated over the displacement in the direction of the force.

$$E = \text{work done}= F \times x$$

In the context of springs and strings, the force is measured as a tension.

$$F=T=-\frac\lambda l x$$

Notice that this tension is dependent upon the displacement, i.e., it is not a constant force when considering work done.

Consider a small change in energy over a small displacement.

$$dE = F(x) \times dx$$

Therefore, integrating over the energy, can be used to calculate the displacement.

$$\int dE = \int F(x) \ dx$$
$$\int dE = \int \frac\lambda l x \ dx$$
$$E + C = \frac\lambda l \int  x \ dx$$
$$E + K = \frac\lambda l \frac12 x^2$$

At no point do we ever care about absolute/total energy, only ever energy change relative to our system (gain/lost/transferred), therefore, without loss of generality, we can ignore the constant $K$.

$$E = \frac {\lambda x^2} {2l}$$

```ad-example
An elastic string has natural length $1.4\ m$ and modulus of elasticity $6\ N$. Find the energy stored in the string when its length is $1.6\ m$

$$E=\frac{6\times0.2^2}{2\times1.4}=0.0857\ J$$
```

Inside a closed system, the energy will be conserved.

$$\text{initial energy} = \text{final energy}$$

`{ \color{red} }`

$${ \color{red} \text{work done}} + { \color{aquamarine} E_k}+{ \color{pink} E_{GP}}+{ \color{yellow} E_{EP}}={ \color{red} \text{work done}} + { \color{aquamarine} E_k}+{ \color{pink} E_{GP}}+{ \color{yellow} E_{EP}}$$

$${ \color{red} \text{driving force}\times(dx)} + { \color{aquamarine} \frac12 mv_0^2}+{ \color{pink} mgh_0}+{ \color{yellow} \frac{\lambda x_0^2}{2l}}={ \color{red} \text{resitive force}\times(dx)} + { \color{aquamarine} \frac12 mv_1^2}+{ \color{pink} mgh_1}+{ \color{yellow} \frac{\lambda x_1^2}{2l}}$$

```ad-warning
Not only does a compressed string have no force, it also stores no potential energy.

In more blunt terms, you cannot compress a string.
```

```ad-example
A particle of mass $0.5\ kg$ is attached to one end of an elastic string, of natural length $2\ m$ and modulus of elasticity $19.6\ N$. The other end of the elastic string is attached to a point $O$. The particle is released from the point $O$. Find the greatest distance it will reach below $O$.

$${ \color{red} \text{driving force}\times(dx)} + { \color{aquamarine} \frac12 mv_0^2}+{ \color{pink} mgh_0}+{ \color{yellow} \frac{\lambda x_0^2}{2l}}={ \color{red} \text{resitive force}\times(dx)} + { \color{aquamarine} \frac12 mv_1^2}+{ \color{pink} mgh_1}+{ \color{yellow} \frac{\lambda x_1^2}{2l}}$$

|          | Initial | Final                   |
| -------- | ------- | ----------------------- |
| WD       | $0$     | $0$                     |
| $E_k$    | $0$     | $0$                     |
| $E_{GP}$ | $5h$    | $0$                     |
| $E_{EP}$ | $0$     | $\frac{19.6(h-2)^2}{4}$ |
| Total    | $5h$    | $\frac{19.6(h-2)^2}{4}$ |

$5h = \frac{19.6(h-2)^2}{4}$
$20h = 19.6(h-2)^2$
$$h \neq 0.0410\ m$$
$$h=4.98\ m$$
```

|          | Initial | Final |
| -------- | ------- | ----- |
| WD       |         |       |
| $E_k$    |         |       |
| $E_{GP}$ |         |       |
| $E_{EP}$ |         |       |
| Total    |         |       |

```ad-tip
Two different approaches:

Hooke's Law & $F=ma$
---
This approach makes no reference to velocity and displacement, therefore it is preferable for:
- Most equlibrium problems
- Problems linked to acceleration and forces

Energy
---
The energy approach makes no reference to internal forces or accleration, therefore it is preferable for:
- Most problems which are linked to destance travelled and velocity.
```

```ad-example
A remote controlled car of mass 1kg is rolling down the line of greatest slope of a ramp inclined at 15° to the horizontal at a speed of 3𝑚𝑠^(−1) when it hits a wall. The non-gravitational resistances to motion can be considered to be 20N and constant. On the front of the car is a bumper that can be modelled as a light elastic spring with natural length 0.2m and modulus of elasticity 50N which compresses on impact with the wall. 10cm after hitting the wall how fast will the car be travelling?

![[Hooke's Law 2023-04-24 14.38.54.excalidraw]]

|          | Initial       | Final                       |
| -------- | ------------- | --------------------------- |
| WD       | $0$           | $20\times0.1$               |
| $E_k$    | $\frac12 3^2$ | $\frac12v^2$                |
| $E_{GP}$ | $0$           | $-10 \times 0.1\sin 15$     |
| $E_{EP}$ | $0$           | $\frac{50\times0.1^2}{0.4}$ |
| Total    | $4.5$         | $2+\frac12v^2-\sin 15+1.25$ |

$$\implies v =1.74\ ms^{-1}$$

How far will the car travel before coming to rest?

|          | Initial       | Final                      |
| -------- | ------------- | -------------------------- |
| WD       | $0$           | $20\times x$               |
| $E_k$    | $\frac12 3^2$ | $0$                        |
| $E_{GP}$ | $0$           | $-10 \times x\sin 15$      |
| $E_{EP}$ | $0$           | $\frac{50\times x^2}{0.4}$ |
| Total    | $4.5$         | $20x-10x\sin 15+125x^2$    |

$$\implies x = 13.2\ cm$$

Once the car has come to rest, will it begin to move again?

$$\frac{50}{0.2}\times0.132\stackrel{?}{=}10\sin 15 + 20$$
$$33 \gt 22.6$$

Yes, it moves back up.
```

```ad-tip
In a dynamic mass-spring system:
- The maximum displacement occurs when velocity is zero.
- The maximum velocity when accleration is zero.
```

```ad-example
One end of a light elastic string, of natural length 0.5m and modulus of elasticity 20N, is attached to a fixed point A. The other end is attached to a particle of mass 2kg. The particle is held at a point which is 1.5m below A and released from rest. Find: 
- The initial acceleration of the particle 
- The maximum speed.

![[Hooke's Law 2023-04-24 15.34.25.excalidraw]]

$$\frac{20}{0.5}-20=2a$$
$$a=10\ ms^{-1}$$

THe point of maximum velocity will occur when acceleration is $0$. Acceleration will be zero when the forces are balanced. The weight force is constant at $20\ N$, therefore, we can calculate the extension in the spring.

$$40x=20 \implies x = 0.5$$

|          | Initial | Final          |
| -------- | ------- | -------------- |
| WD       | $0$     | $0$            |
| $E_k$    | $0$     | $v^2$          |
| $E_{GP}$ | $0$     | $20\times 0.5$ |
| $E_{EP}$ | $20$    | $20\times0.25$ |
| Total    | $20$    | $v^2+15$       | 

$$5=v^2 \implies v = \sqrt{5}$$
```

|          | Initial | Final          |
| -------- | ------- | -------------- |
| WD       | $0$     | $0$            |
| $E_k$    | $0$     | $v^2$          |
| $E_{GP}$ | $0$     | $20\times 0.5$ |
| $E_{EP}$ | $20$    | $20\times0.25$ |
| Total    | $20$    | $v^2+15$       | 

# Combination of Problems

```ad-example
One end of a light elastic string, of natural length $a$ and modulus of elasticity $3\ mg$, is attached to a fixed point $O$ on a smooth horizontal plane.
```

```ad-example
a particle of mass 0.5kg moves in a straight horizontal line. When the speed of P is 𝑣𝑚𝑠^(−1), the resultant force acting on P is a resistance of magnitude 3𝑣 N. Find the distance moved by P as it slows down from 12𝑚𝑠^(−1) to 6𝑚𝑠^(−1).
```