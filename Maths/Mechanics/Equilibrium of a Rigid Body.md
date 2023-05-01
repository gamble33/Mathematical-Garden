# Definitions
```ad-definition
**Particles** are point masses.

In a 3-dimensional space, a particle has 3 degrees of freedom.
In a 2-dimensional space, a particle has 2 degrees of freedom.
```

```ad-definition
**Rods** or **beams** are one dimensional bodies with a mass. They expereince movement and forces.

In a 3-dimensional space, a rod has 5 degrees of freedom.
In a 2-dimensional space, a rod has 3 degrees of freedom.
```

```ad-definition
A **lamina** is a two dimensional body with a mass. They expereince movement and forces.

In a 3-dimensional space, a lamina has 6 degrees of freedom.
In a 2-dimensional space, a lamina has 3 degrees of freedom.
```

```ad-definition
A **body** refers to any fixed amount of matter. Bodies can be volumuous, 3D objects.
```

```ad-definition
A **rigid body** is a body which does not deform. It will not break.
```

```ad-definition
The **center of mass (COM)** is a modelling tool which simplifies a body such that all the internal forces act through the single point, $(\overline{x}, \overline{y})$.

An external forces acting on the body at the center of mass will cause a linear acceleration but not an angular acceleration.
```
# Moments
The **moment** of a force measures the **turning effect** of the force on the body.
$$\text{moment of force}=|\text{force}\times\text{displacement}|$$
where:
- $\text{force}\times\text{displacement}$ is the cross product of the displacement and force.

```ad-example
The diagram shows two force acting on a lamina. Find the moment of each of the forces about the point $P$.

![[Pasted image 20230329105336.png]]

Moment of $5\ N$ force:
$$=5\times2=10\ Nm\ \text{clockwise}$$

Moment of $8\ N$ force:
$$=2\times8\cos40^\circ=12.3\ N m\  \text{anti-clockwise}$$
```

The resultant moment, $M_A$ about the point $A$:
$$M_A=\sum |F_i\times s_i|$$
where:
- $F_i$ is a force acting at point $i$.
- $s_i$ is the displacement from the point of action (of force $F_i$) to the point $A$.

```ad-example
The diagram shows two forces acting on a lamina. Calculate the resultant moment about the point $P$.

![[Pasted image 20230329110702.png]]

Moment of the $7\ N$ force:
$$=7\times8\sin25=23.7\ Nm\ \text{clockwise}$$

Moment of the $4\ N$ force:
$$=4\times8\sin35=18.4\ Nm\ \text{anti-clockwise}$$

Resultant Moment:
$$=5.3\ Nm\ \text{clockwise}$$

```
# Centres of Mass
## Rods
```ad-example
Sam and Tamsin are sitting on a non-uniform plan $𝐴𝐵$ of mass $25\ kg$ and length $4\ m$. The plank is pivoted at $𝑀$, the midpoint of $𝐴𝐵$. The centre of mass of $𝐴𝐵$ is at $𝐶$ where $𝐴𝐶$ is $1.8$. Sam has mass $35\ kg$. Tamsin has mass $25\ kg$ and sits at $𝐴$. Where must Sam sit for the plank to be horizontal?

calculating moments about point $M$:
$$0.2\times250+2\times250=d\times350$$
$$x=3.57\ m$$
```

$$\sum^n_{i=1}m_ix_i=\overline{x}\sum^n_{i=1}m_i$$
$$\sum F_ix_i = \text{resultant moment}$$
$\text{LHS}=\text{sum of moments} \implies \text{resultant moment}$
COM is the imaginary point through which all forces appear to act.
$$\overline{x}=\sum F_i$$
$\text{resultant moment}=\text{COM}\times\sum m$
$$\therefore \sum F_i x_i = \overline{x}\sum F_i$$
dividing by acceleration,
$$\sum m_i x_i = \overline{x}\sum m_i$$
$$\overline{x}=\frac{\sum m_i x_i}{\sum m_i}$$
where:
- $\overline x$ is the centre of mass

```ad-example
A system of $3$ particles with masses 2kg, 5kg and 3kg are placed along the 𝑥-axis at the points (3,0), (4,0) and (6,0) respectively. Find the centre of mass of the system.

$$\overline{x}=\frac{2\times3+5\times4+3\times6}{2+5+3}$$
$$=4.4$$
```
## Lamina
$$\overline{x}=\frac{\sum m_i x_i}{\sum m_i}$$
$\overline x$ is a displacement vector, therefore by extending the formula derived, it can be rewritten as
$$\left(\begin{matrix}\overline{x}\\\overline{y}\end{matrix}\right)\overline{x}=\frac{\sum m_i \left(\begin{matrix}x_i\\y_i\end{matrix}\right)}{\sum m_i}$$

```ad-example
Find the co-ordinates of the centre of mass of the following system of particles: 2kg at (1,2); 3kg at (3,1); 5kg at (4,3)

$$\overline{x}=(3.1,2.2)$$
```

```ad-note
Sometimes the origin point will have to be chosen. Oftentimes, a sensible origin is a given point (with a mass).

The most bottom-left point will typically yield a more peaceful experience (working with mostly positive numbers).
```

```ad-important
For uniform lamina:

- If there is a line of symmetry, the center of mass must be on it.
- If there are two lines of symmetry, the center of mass must lay on the intersection.
- If there is a rotational symmetry, the center of mass will be on the point of rotational symmetry.

*Justification*: Any line drawn through the center of mass must divide the lamina into two equal masses.
```

### Triangles
Centre of mass for triangular lamina:
$$\overline{x}=\frac23\ \text{along median from vertex}$$
#### Method 1: The Formula
1. Identify a vertex and a midpoint of an opposite line.
2. Identify the vector connecting them.
3. Find $\frac23$ of that vector and add this to the position vertex.
#### Method 2: Intersecting Medians
1. Identify a median.
2. Identify a second median.
3. Identify the point of intersection.
#### Method 3: Averaging Co-ordinates
1. Identify the coordinates of the three vertices.
2. Find the arithmetic mean of these three coordinates.
#### Method 4: Parallel Lines
1. Identify the equation of the line of the base.
2. Translate this line $\frac13$ of the distance between the base and the apex.
3. Identify the equation of the line of another base.
#### Method 5: Symmetry
1. Identify two lines of symmetry.
2. Identify the point of intersection.

### Sector of a Circle
The centre of mass of a sector of a circle must lie on the line of symmetry. This will be at half the angle of the sector.

Consider a sector with angle $2\alpha$ and radius $r$:
![[Pasted image 20230330101837.png]]
$$\text{dist of COM from vertex}=\frac{2r\sin\alpha}{3\alpha}$$

```ad-warning
The angle given/measured is $2\alpha$ in most cases.
```

```ad-danger
This formula only works in $\text{rad}$ (radians).
```

#### Proof
Consider a sector who's line of symmetry is on the $x$-axis. Using symmetry, we can consider the top half only and calculate the centre of mass from the $y$-axis.
$$f(x)=\left\{\begin{matrix}x\tan\alpha,&(0,r\cos\alpha)\\\sqrt{r^2-x^2},&(r\cos\alpha, r) \end{matrix}\right\}$$
$$xf(x)=\left\{\begin{matrix}x^2\tan\alpha,&(0,r\cos\alpha)\\x\sqrt{r^2-x^2},&(r\cos\alpha, r) \end{matrix}\right\}$$
btw constant of integration is ignored because we are about to perform definite integration.
$$\int xf(x)\ dx=\left\{\begin{matrix}\frac13x^3\tan\alpha,&(0,r\cos\alpha)\\-\frac13(r^2-x^2)^{\frac32},&(r\cos\alpha, r) \end{matrix}\right\}$$

$$\overline{x}=\frac{\int^b_a xy\ dx}{\int^b_a y\ dx}$$
$$\overline{x}=\frac{\frac13r^3\cos^3\alpha\tan\alpha+\frac13(r^2-r^2\cos^2\alpha)^\frac32}{\frac12\alpha r^2}$$
$$=\frac{\frac13r^3\cos^3\alpha\tan\alpha+\frac13r^3(\sin^2\alpha)^\frac32}{\frac12\alpha r^2}$$
$$=\frac{\frac13r^3\cos^3\alpha\tan\alpha+\frac13r^3\sin^3\alpha}{\frac12\alpha r^2}$$
$$=\frac{\frac23r\cos^3\alpha\tan\alpha+\frac23r\sin^3\alpha}{\alpha}$$
$$=\frac{\frac23r\sin\alpha(\cos^2\alpha+\sin^2\alpha)}{\alpha}$$
$$=\frac{\frac23r\sin\alpha}{\alpha}$$
$$=\frac{2r\sin\alpha}{3\alpha}$$

#Todo 

```ad-example
A cheeseboard in the shape of a sector (angle ($2\alpha$): $100^\circ$), radius $9\ cm$, is shown below. If the board is modelled as a uniform lamina, find the distance of the centre  of mass from the vertex, $O$.

$$=\frac{2\times9\times\sin50^\circ}{3\times50}=5.27\ cm$$
```

### Composite Shapes
1. Calculate centre of masses of individual shapes.
	1. The mass of the shapes is $\rho\times A_{\text{shape}}\equiv\text{density}\times\text{area}$
2. Consider these as point masses.
3. Find the centre of mass of these point masses (summation formula).

```ad-tip
**PRO TIP**
If a composite shape is given such that a well-defined shape is removed from it:

The area/volume of the removed section can be calculated and treated as a negative mass.
```

```ad-example
Find the centre of mass.
![[Pasted image 20230330105937.png]]

Assume $D$ is the point $(0,0)$

Part 1: Rectangle
$$\text{COM}=(5,5)$$
$$\text{relative mass}=100$$

Part 2: Semi-circle
$$\text{COM}=(5,7.88)$$
$$\text{relative mass}=\frac{5^2\pi}{2}=-39.3$$

$$\text{COM}=\frac{5\times100+7.88\times-39.3}{60.7}=(5,3.15)$$
```

### Arbitrary Lamina Composed of a Function
Consider a lamina bound by the $x$-axis, vertical lines $x=a,x=b$, and a function $y=f(x)$.

$$\overline{x}=\frac{\int^b_a xy\ dx}{\int^b_a y\ dx}$$
$$\overline{y}=\frac{\int^b_a y^2\ dx}{2\int^b_a y\ dx}$$

## Solids
### Derivations
Consider a solid formed by a revolution of the curve $y=f(x)$ about the $x$-axis bound by the planes at $x=a$ and $x=b$.
![[Pasted image 20230330124010.png]]
Consider a small disc, $D$, of width $\delta x$ at position $x$.

$$\text{volume of disc }D=\pi y^2 \delta x$$
$$\text{mass of disc }D=\rho\pi y^2 \delta x$$
$$\text{moment of the mass of disc D at y-axis}=x\rho\pi y^2 \delta x$$
$$\text{moment of the mass of disc D at x-axis}=0$$

$$\text{sum of moments about y-axis}=\rho\pi\int^b_a xy^2\ dx$$

$$\text{total volume}=\pi\int^b_ay^2\ dx$$
$$\implies \text{total mass}=\rho\pi\int^b_ay^2\ dx$$

$$\text{COM}=\frac{\rho\pi\int^b_a xy^2\ dx}{\rho\pi\int^b_ay^2\ dx}$$
$$=\frac{\int^b_a xy^2\ dx}{\int^b_ay^2\ dx}$$

```ad-tip
If the shape is made by rotation about the $\text{y-axis}$, then the same formula is valid but $x$ and $y$ are switched.
![[Pasted image 20230330125002.png]]
$$\text{COM}=\frac{\int^b_a x^2y\ dy}{\int^b_ax^2\ dy}$$
```


### Hemisphere
Consider a hemisphere formed by the equation given below.
$$x^2+y^2=R^2, x\in [0,R]$$
The hemisphere is rotated by $2\pi$ about the $\text{x-axis}$.

$$\text{total mass}=\frac23\pi R^3$$
$$y^2=R^2-x^2$$
$$\implies \text{total moment}=\pi\int^{R}_{0}xR^2-x^3\ dx = \pi\left[\frac12R^2x^2-\frac14x^4\right]^R_0$$
$$=\pi\left(\frac12R^4-\frac14R^4\right)=\pi\frac14R^4$$
$$\text{COM}=\frac{\frac14R^4}{\frac23 R^3}=\frac{3R}{8}$$

### Solid Cone
Consider a solid cone of height $h$ and radius $R$.
![[Pasted image 20230330130423.png]]
$$\text{total mass}=\pi R^2 \frac h3$$
$$y=\frac R h x,\space x\in[0,h]$$
$$y^2=\frac {R^2} {h^2} x^2$$
$$\implies \text{total moment}=\pi\frac {R^2} {h^2} \int^h_0 x^3\ dx=\frac{\pi R^2}{4h^2}\left[x^4\right]^h_0$$
$$\frac14\pi R^2 h^2$$
$$\implies \text{COM}=\frac{\frac14\pi R^2 h^2}{\pi R^2 \frac h3}=\frac34h$$
The distance $\frac34 h$ is the distance from the vertex (apex).

### Composite Solids
1. Calculate centre of masses of individual solids.
	1. The mass of the solids is $\rho\times V_{\text{shape}}\equiv\text{density}\times\text{volume}$
2. Consider these as point masses.
3. Find the centre of mass of these point masses ($\overline{x}=\frac{\text{total moment}}{\text{total mass}}=\frac{\sum x\times m}{\sum m}$).

```ad-example
A uniform solid circular cone of height 2R and base radius R is joined at its base to the base of a uniform solid hemisphere. The centres of their bases coincide at O and their axes are collinear. The radius of the hemisphere is 2R. Find the position of the center of mass of the composite body if the cone has four times the density of the hemisphere.

![[Pasted image 20230403130657.png]]

> [!danger]
> Notice that the densities are not the same. However, they are proportional.

$$\text{displacement(COM of hemisphere, O)}=-\frac34R$$
$$\text{mass of hemisphere}=\rho\frac{16}3\pi R^3$$
$$\text{displacement(COM of cone, O)}=\frac14\times2R=\frac12R$$
$$\text{mass of cone}=\frac {8R} 3 \rho \pi R^2=\frac83\rho\pi R^3$$
$$\overline{x}=\frac{\rho\pi R^4(\frac43-\frac{12}{3})}{8\rho\pi R^3}$$
$$\overline{x}=\frac{R(\frac43-\frac{12}{3})}{8}=-\frac13R$$
```

## Frameworks
```ad-danger
Questions are written to mislead you. Be sure to double check if the shape is a framework or a lamina.

A framework is the perimeter.

A lamina is the area.
```

### Composite Shapes
1. Calculate centre of masses of individual shapes.
	1. The mass of the shapes is $\rho\times L_{\text{shape}}\equiv\text{density}\times\text{length}$
2. Consider these as point masses.
3. Find the centre of mass of these point masses (summation formula).

### Rods
$$\text{COM}=\text{mid-point}$$

```ad-example
![[Pasted image 20230330112308.png]]
Find the distance of the centre of mass of the frame from $BC$.

Assume an origin at centre of $BC$.

$AB$:
$$B(-6,0), A(0,8)$$
$$\implies \text{mid-point}=(\frac{-6+0}{2},\frac{0+8}{2})=(-3,4)$$
$$\text{COM}_{AB}=(-3,4)$$
$$\text{relative mass}=1$$
similarly, $AC$:
$$\text{COM}_{AC}=(3,4)$$
$$\text{relative mass}=1$$

$BC$:
$$\text{COM}_{BC}=(0,0)$$
$$\text{relative mass}=1.2$$

$$\therefore \text{COM}_y=\frac{4+4+0\times1.2}{3.2}$$
$$\therefore \text{COM}=(0,2.5)$$
$$\implies \text{distance from }BC=2.5$$
```

### Arcs
$$\text{distance of COM from centre}=\frac{r\sin\alpha}{\alpha}$$

```ad-warning
The angle given/measured is $2\alpha$ in most cases.
```

```ad-danger
This formula only works in $\text{rad}$ (radians).
```

#### Proof
Consider a circular arc with radius $r$ and angle $2\alpha$.
![[Pasted image 20230403124335.png]]
$$\text{circumference of arc with angle }\alpha=\frac{\alpha}{2\pi}2\pi r=\alpha r$$
$$\text{total mass}=\rho\alpha r$$
$$\text{moment about y-axis}=\rho\delta\alpha r \times r\cos\alpha=\rho r^2 \cos\alpha \times\delta \alpha$$
$$\text{total moment}=\rho r^2\int^\alpha_0 \cos\alpha\ d\alpha$$
$$=\rho r^2 \sin\alpha$$
$$\text{dist(COM, y-axis)}=\frac{\rho r^2 \sin\alpha}{\rho\alpha r}$$
$$=\frac{r\sin\alpha}{\alpha}$$

```ad-example
A pole of length $3\ m$ is bent to make a rigid curtain pole for a bay window. The window followed the shape of the arc of a circle radius $3\ m$. If the pole is modelled as thin and uniform calculate how far the centre of mass is from the pole. Give your answer in meters to $5$ decimal places.

$$\text{arc length}=\text{radius}\implies 2\alpha=1\ \text{rad}$$
$$\implies \text{distance of COM from centre}=\frac{3\sin\frac12}{\frac12}=2.876553232\ m$$
$$\implies \text{distance of COM from pole}=1-2.876553232=0.12345\ m$$
```

## Shells
Consider a hollow shell (surface/2D manifold) formed by rotating the line $y=f(x)$ by $2\pi$ around the $x$-axis.
![[Pasted image 20230403115145.png]]
$$\text{surface area of cylinder}=2\pi y\Delta x$$
$$\text{total surface area}=2\pi\int^b_a y\ dx$$
$$\text{total mass}=2\pi\rho\int^b_a y\ dx$$
$$\text{moment of C about y-axis}=2\pi\rho y\Delta x \times x$$
$$\text{total moment}=2\pi\rho\int^b_a yx\ dx$$
$$\text{distance of COM from y-axis}=\frac{2\pi\rho\int^b_a yx\ dx}{2\pi\rho\int^b_a y\ dx}$$
$$=\frac{\int^b_a yx\ dx}{\int^b_a y\ dx}$$
### Conic Shell
Consider a conic shell formed by rotating the line $y=\frac R h x$ by $2\pi$ around the $x$-axis.
![[Pasted image 20230403120349.png]]
$$\text{dist(COM, y-axis)}=\frac{\int^b_a yx\ dx}{\int^b_a y\ dx}$$
$$=\frac{\int^h_0 \frac R h x^2\ dx}{\int^h_0 \frac R h x\ dx}$$
$$=\frac{\frac R h\int^h_0  x^2\ dx}{\frac R h\int^h_0  x\ dx}$$
$$=\frac{\int^h_0  x^2\ dx}{\int^h_0  x\ dx}$$
$$=\frac{\frac13[x^3]^h_0}{\frac12[x^2]^h_0}$$
$$=\frac{\frac13h^3}{\frac12h^2}$$
$$=\frac23h$$
The centre of mass of a hollow conic shell is always $\frac23$ of the distance from the apex to the base.

### Hemispherical Shell
Consider a hollow, hemispherical shell with radius $R$. This composed of the equation $x^2+y^2=R^2$ rotated by $\pi$  around the $x$-axis.
![[Pasted image 20230403121524.png]]
$$\text{surface area of sphere}=4\pi r^2$$
$$\text{total mass}=2\rho\pi R^2$$
$$\text{total moment}=2\pi\rho\int^b_a yx\ dx$$
$$=2\pi\rho\int^R_0 x\sqrt{R^2-x^2}\ dx$$
$$\text{dist(COM, y-axis)}=\frac{2\pi\rho\int^R_0 x\sqrt{R^2-x^2}\ dx}{2\rho\pi R^2}$$
$$=\frac{\int^R_0 x\sqrt{R^2-x^2}\ dx}{R^2}$$
$$=\frac{-\frac13[(R^2-x^2)^{\frac32}]^R_0}{R^2}$$
$$=\frac{\frac13R^3}{R^2}$$
$$=\frac13R$$
The distance of the centre of mass from the centre of the hemisphere is $\frac13$ of the radius of the hemisphere.

## Variable Density
### Solid
Consider a density formula $\rho_x$ that is dependent on $x$ of a shape described by $f(x)$ rotated about the $\text{x-axis}$.
![[Pasted image 20230330124010.png]]
Consider a small disc, $D$, of width $\delta x$ at position $x$.

$$\text{volume of disc }D=\pi y^2 \delta x$$
$$\text{mass of disc }D=\rho(x)\pi y^2 \delta x$$
$$\text{moment of the mass of disc D at y-axis}=x\rho(x)\pi y^2 \delta x$$
$$\text{moment of the mass of disc D at x-axis}=0$$

$$\text{sum of moments about y-axis}=\pi\int^b_a \rho(x)xy^2\ dx$$

$$\text{total volume}=\pi\int^b_ay^2\ dx$$
$$\implies \text{total mass}=\pi\int^b_a\rho(x)y^2\ dx$$

$$\text{COM}=\frac{\pi\int^b_a \rho(x)xy^2\ dx}{\pi\int^b_a\rho(x)y^2\ dx}$$
$$=\frac{\int^b_a xy^2\ dx}{\int^b_ay^2\ dx}$$

# Hanging
If a rigid body is freely suspended from a point then the centre of mass will rest in equilibrium below the point of suspension.

```ad-example
The lamina is supsended freely from the point $D$ and hangs at rest.
Find, in degrees, the angle between $CD$ and the vertical, $\theta$.
![[Pasted image 20230330105937.png]]

Assume $D$ is the point $(0,0)$

Part 1: Rectangle
$$\text{COM}=(5,5)$$
$$\text{relative mass}=100$$

Part 2: Semi-circle
$$\text{COM}=(5,7.88)$$
$$\text{relative mass}=\frac{5^2\pi}{2}=-39.3$$

Part 3: Center of mass
$$\text{COM}=\frac{5\times100+7.88\times-39.3}{60.7}=(5,3.15)$$

Part 4: Angle

$$\theta=\arctan{\frac{3.15}{5}}=32.2^\circ$$
```

```ad-example
![[Pasted image 20230403150116.png]]
$$\text{mass of smaller cone}=\pi r^2 \frac{h}{3} \rho$$
$$\text{mass of larger cone}=\pi r^2 \frac{kh}{3} \rho$$
$$\text{displacement(COM of smaller cone, O)}=-\frac14 h$$
$$\text{displacement(O, COM of larger cone)}=\frac14 kh$$
$$\text{COM}=\frac{\pi r^2 \rho h^2(k^2-1)\frac1{12}}{\frac{h(k+1)}{3}\pi r^2 \rho}$$
$$\text{COM}=\frac14h(k-1)$$

$$\tan 30^\circ=\frac{1}{4r}h(k-1)$$
$$\frac1{\sqrt{3}}=\frac{1}{4r}h(k-1)$$
$$\frac{4r}{h\sqrt{3}}=k-1$$
$$k=\frac{4r}{h\sqrt{3}}+1$$
```

# Sliding or Toppling
In order to determine if a shape will slide, we simply need to compare the force of friction with the force of action. Friction is being measured as $\mu R$.

In order to determine if a shape will topple (rotate about one of the edges of its base) we need to consider the location of the centre of mass with the base. If the centre of mass is vertically above the base, the shape should remain stable. If its centre of mass is outside of the base, it will topple. 


```ad-definition
**Line of Weight (LOW)** is the vertical line coming down from a centre of mass.
```

```ad-definition
A **footprint** is the area or line connecting two shapes/bodies.
```

## Horizontal Plane. 
```ad-example
A uniform cube of mass M and side length 2a sits on a horizontal plane. The coefficient of friction between the cube and the plane is 𝜇. A horizontal force P is applied to the cube at a height 𝑥 above the plane which is just sufficient to break equilibrium. Calculate, in terms of a and 𝜇, the range of values of 𝑥 that would result in equilibrium being broken by sliding and those that would result in equilibrium being broken by toppling.

![[Pasted image 20230403160111.png]]

$$\text{resultant force}=\mu Mg-P$$
Consider the situation on the point of sliding:
$$P \gt \mu Mg$$
Consider the situation on the point toppling:
$$\mu Mg \geq P$$
$$\text{resultant moment about C}=Px - aMg$$
$$Px-aMg\gt 0$$
$$P\gt\frac{aMg}{x}$$
```

## Inclined Planes
|                      | Sliding                                                               | Toppling                                                    |
| -------------------- | --------------------------------------------------------------------- | ----------------------------------------------------------- |
|                      | Compare the parallel components of weight with the value of friction. | Compare the line of weight with the footprint of the shape. |
| Equilibrium          | $$\mu R \gt mg\sin\theta$$                                            | The line of weight is within the footprint of the shape.    |
| Limiting Equilibrium | $$\mu R=mg\sin\theta$$                                                | The line of weight is through the edge of the footprint.    |
| Equilibrium Broken   | $$\mu R \lt mg\sin\theta$$                                            | The line of weight is outside of the footprint.             | 

```ad-example
A component is formed by joining a solid cylinder of uniform density 𝜌, radius r and height 2r to a solid cone of uniform density 𝑘𝜌, radius r and perpendicular height 4r. The cone sits on top of the cylinder such that their circular faces coincide on a plane inclined at 25°. The plane is sufficiently rough to prevent the component sliding down the plane. Find the range of values of the positive constant 𝑘 such that the component will remain in equilibrium.

![[Equilibrium of a Rigid Body 2023-04-04 14.32.55.excalidraw]]

$$\text{mass of cylinder}=\rho\times2\pi r^3$$
$$\text{mass of cone}=k\rho\times\frac43\pi r^3$$
$$\text{displacement(COM cone, centre base)}= 3r$$
$$\text{displacement(COM cylinder, centre base)}=r$$
$$\text{displacement(COM, centre base)}=\frac{r(1+2k)}{1+\frac{2k}{3}}$$
$$\tan65\gt\frac{3(1+2k)}{3+2k}$$
$$k\lt \frac{3(\tan65-1)}{2(3-\tan65)}$$
$$k\lt2.01$$
```