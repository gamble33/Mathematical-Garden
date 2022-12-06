#Maths #Todo

# Vectors
A vector has two properties

## Operations
### Adding
The corresponding components of each vector are summed.
$$\left(\begin{matrix}a\\b\end{matrix}\right)+\left(\begin{matrix}x\\y\end{matrix}\right)=\left(\begin{matrix}a+x\\b+y\end{matrix}\right)$$
### Scalar (Dot) Product
$${\mathbf a}\bullet{\mathbf{}b}=\cos\theta\times|{\mathbf a}||{\mathbf b}|$$
$$\left(\begin{matrix}a\\b\\c\end{matrix}\right)\bullet\left(\begin{matrix}x\\y\\z\end{matrix}\right)=ax+by+cz$$
### Cross Product
Also known as the vector product.
$${\mathbf{a}}\times{\mathbf{b}}=|{\mathbf{a}}||{\mathbf{b}}|\sin(\theta) {\mathbf{\hat{n}}}$$

#### Properties
> [!Warning]
> The cross product is [[Anticommutative]]. $${\mathbf{b}}\times{\mathbf{a}}=-{\mathbf{a}}\times{\mathbf{b}}$$

> [!Note]
> The vector product is [[Distributive|distributive]] over addition.

#### Result

The result of the cross product, ${\mathbf{a}}\times{\mathbf{b}}$, is a vector which is perpendicular to both vectors $\mathbf{a}$ and $\mathbf{b}$. 
> [!Note]
> The direction is perpendicular in the direction of the right hand rule.
> ![[right_hand_rule.png#invert_B|300]]

The magnitude of the result is equal to $|{\mathbf{a}}||{\mathbf{b}}|\sin(\theta)$.

#### Basis Vectors

> [!Note]
> Any vector that is taken as a vector product with itself will result in $0=\left(\begin{matrix}0\\0\\0\end{matrix}\right)$

$${\bf{i}}\times{\bf{i}}=0=\left(\begin{matrix}0\\0\\0\end{matrix}\right)$$
$${\mathbf{j}}\times{\mathbf{k}}={\mathbf{i}}$$
$${\mathbf{i}}\times{\mathbf{k}}={\mathbf{-j}}$$

> [!Note]
> In three dimensions, the vector product of any two basis vectors will result in $\pm$ the third one. Positive if the operands of the cross product follow alphabetic order, otherwise the result will be negative.

#### Derivation
Given that ${\mathbf{a}}=\left(\begin{matrix}a_1\\a_2\\a_3\end{matrix}\right)$ and ${\mathbf{b}}=\left(\begin{matrix}b_1\\b_2\\b_3\end{matrix}\right)$, determine ${\mathbf{a}}\times{\mathbf{b}}$.

$${\mathbf{a}}\times{\mathbf{b}}=(a_1{\mathbf{i}}+a_2{\mathbf{j}}+a_3{\mathbf{k}})\times(b_1{\mathbf{i}}+b_2{\mathbf{j}}+b_3{\mathbf{k}})$$

Because the vector product is [[Vector#Properties|distributive]], we can multiply out these parenthesized expressions with a grid method.

|                   | $a_1{\mathbf{i}}$                        | $a_2{\mathbf{j}}$                    | $a_3{\mathbf{k}}$                    |
| ----------------- | ---------------------------------------- | ------------------------------------ | ------------------------------------ |
| $b_1{\mathbf{i}}$ | $a_1b_1({\mathbf{i}}\times{\mathbf{i}})$ | $a_2b_1(\mathbf{j}\times\mathbf{i})$ | $a_3b_1(\mathbf{k}\times\mathbf{i})$ |
| $b_2{\mathbf{j}}$ | $a_1b_2({\mathbf{i}}\times{\mathbf{j}})$ | $a_2b_2(\mathbf{j}\times\mathbf{j})$ | $a_3b_2(\mathbf{k}\times\mathbf{j})$ |
| $b_3{\mathbf{k}}$ | $a_1b_3({\mathbf{i}}\times{\mathbf{k}})$ | $a_2b_3(\mathbf{j}\times\mathbf{k})$ | $a_3b_3(\mathbf{k}\times\mathbf{k})$ |

Now simplify the basis vectors.

|                   | $a_1{\mathbf{i}}$     | $a_2{\mathbf{j}}$     | $a_3{\mathbf{k}}$     |
| ----------------- | --------------------- | --------------------- | --------------------- |
| $b_1{\mathbf{i}}$ | $0$                   | $-a_2b_1{\mathbf{k}}$ | $a_3b_1{\mathbf{j}}$  |
| $b_2{\mathbf{j}}$ | $a_1b_2{\mathbf{k}}$  | $0$                   | $-a_3b_2{\mathbf{i}}$ |
| $b_3{\mathbf{k}}$ | $-a_1b_3{\mathbf{j}}$ | $a_2b_3{\mathbf{i}}$  | $0$                   |

$$=(a_2b_3-a_3b_2){\mathbf{i}}+(a_3b_1-a_1b_3)\mathbf{j}+(a_1b_2-a_2b_1){\mathbf{k}}$$

If we compose the following [[Matrices|matrix]]:
$$\left[\begin{matrix}{\mathbf{i}}&{\mathbf{j}}&{\mathbf{k}}\\a_1&a_2&a_3\\b_1&b_2&b_3\end{matrix}\right]$$
Then, calculating the [[Matrices#Determinant|determinant]] of this $3\times3$ matrix will yield the vector product.

$$\text{Vector Product:}\space {\mathbf{a}}\times{\mathbf{b}}=|{\mathbf{a}}||{\mathbf{b}}|\sin(\theta){\hat{\mathbf{n}}}=\text{det}\left[\begin{matrix}{\mathbf{i}}&{\mathbf{j}}&{\mathbf{k}}\\a_1&a_2&a_3\\b_1&b_2&b_3\end{matrix}\right]=\left[\begin{matrix}a_2b_3-a_3b_2\\a_3b_1-a_1b_3\\a_1b_2-a_2b_1\end{matrix}\right]$$

#### Applications
##### Areas of Shapes
$${\mathbf{a}}\times{\mathbf{b}}=|{\mathbf{a}}||{\mathbf{b}}|\sin(\theta)\hat{\mathbf{n}}$$
Know that $|\hat{\mathbf{n}}|=1$. 
$$\therefore|{\mathbf{a}}\times{\mathbf{b}}|=|{\mathbf{a}}||{\mathbf{b}}|\sin\theta$$
**OMFG, it's double the area of a triangle.** To be more precise, $|{\mathbf{a}}\times{\mathbf{b}}|$ is the area of a parallelogram. 

### Triple Scalar Product
#### Definition
The triple scalar product of three vectors is the dot product of one of the vectors with the cross product of the other two.
$$\text{suppose}\space {\mathbf{a}}=\left(\begin{matrix}a_1\\a_2\\a_3\end{matrix}\right)=a_1{\mathbf{i}}+a_2{\mathbf{j}}+a_3{\mathbf{k}}$$
Then the triple scalar product is
$${\mathbf{a}}\bullet({\mathbf{b}}\times{\mathbf{c}})=a_1(b_2c_3-b_3c_2)+a_2(b_3c_1-b_1c_3)+a_3(b_1c_2-b_2c_1)$$
$$=\text{det}\left[\begin{matrix}a_1&a_2&a_3\\b_1&b_2&b_3\\c_1&c_2&c_3\end{matrix}\right]$$
#### Properties
##### Scalar Product Commutativity
$${\mathbf{a}}\bullet({\mathbf{b}}\times{\mathbf{c}})\equiv({\mathbf{b}}\times{\mathbf{c}})\bullet{\mathbf{a}}$$
##### Circular Shift
$${\mathbf{a}}\bullet({\mathbf{b}}\times{\mathbf{c}})\equiv{\mathbf{c}}\bullet({\mathbf{a}}\times{\mathbf{b}})$$
##### Operator Transposition
$${\mathbf{a}}\times{\mathbf{b}}\bullet{\mathbf{c}}\equiv {\mathbf{a}}\bullet{\mathbf{b}}\times{\mathbf{c}}$$
##### Reverse Cycle
$$-{\mathbf{a}}\bullet({\mathbf{b}}\times{\mathbf{c}})={\mathbf{c}}\bullet({\mathbf{b}}\times{\mathbf{a}})$$
###### Derivation
$${\mathbf{c}}\bullet({\mathbf{b}}\times{\mathbf{a}})=({\mathbf{c}}\times{\mathbf{b}})\bullet{\mathbf{a}}={\mathbf{a}}\bullet({\mathbf{c}}\times{\mathbf{b}})$$
Vector products are [[Vector#Properties|anticommutative]], therefore:
$${\mathbf{c}}\times{\mathbf{b}}=-{\mathbf{b}}\times{\mathbf{c}}$$
$$\therefore$$
$$-{\mathbf{c}}\bullet({\mathbf{b}}\times{\mathbf{a}})={\mathbf{a}}\bullet({\mathbf{b}}\times{\mathbf{c}})$$
##### Repeated Vector
$${\mathbf{a}}\bullet({\mathbf{a}}\times{\mathbf{b}})=0$$
By using the [[Vector#Triple Scalar Product#Operator Transposition|operator transposition]] property, we can show that
$${\mathbf{a}}\bullet({\mathbf{a}}\times{\mathbf{b}})=({\mathbf{a}}\times{\mathbf{a}})\bullet{\mathbf{b}}$$
[[Vector#Cross Product#Basis Vectors|Any vector that is taken as a cross product with itself is equal to 0]], therefore
$${\bf{a}}\times{\mathbf{a}}=0$$
$$\therefore{\mathbf{a}}\bullet({\mathbf{a}}\times{\mathbf{b}})=0$$
#### Applications
##### [[Parallelepiped#Volume|Volume]] of a [[Parallelepiped]]
$$V={\mathbf{a}}\bullet({\mathbf{b}}\times{\mathbf{c}})$$
![[Pasted image 20220929114917.png]]
[[Vector#Cross Product#Areas of Shapes|We know the cross product of two vectors gives a vector with magnitude that is the area of the parallelogram that the vectors make]]. I.e., ${\mathbf{b}}\times{\mathbf{c}}$ is a vector which has magnitude which is equal to the area of the base and a direction (unit vector $\hat{\mathbf{n}}$) that is equal to the direction of $h$. (The direction is perpendicular).

To find the height, $h$, we use the scalar product. This is because the scalar product, ${\mathbf{a}}\bullet\hat{\mathbf{n}}$, is the projection of $\mathbf{a}$ onto $\hat{\mathbf{n}}$. Because, $\hat{\mathbf{n}}$ is a unit vector, its length is irrelevant.
$${\mathbf{a}}\bullet\hat{\mathbf{n}}=h$$

Because, ${\mathbf{b}}\times{\mathbf{c}}=\text{area of base}\times\hat{\mathbf{n}}$, $$\text{volume}={\mathbf{a}}\bullet({\mathbf{b}}\times{\mathbf{c}})$$.

##### Volume of a Tetrahedron
For a similar reason as the [[Vector#Triple Scalar Product#Applications#Parallelepiped Volume Volume of a Parallelepiped|volume of a parallelepiped]],
$$V=\frac{1}{6}{\mathbf{a}}\bullet({\mathbf{b}}\times{\mathbf{c}})$$

**Example**
![[Pasted image 20220929123819.png]]
$${\mathbf{b}}\times{\mathbf{c}}=\left(\begin{matrix}0\\5\\5\end{matrix}\right)$$
$${\mathbf{a}}\bullet({\mathbf{b}}\times{\mathbf{c}})=\left(\begin{matrix}1\\1\\0\end{matrix}\right)\bullet\left(\begin{matrix}0\\5\\5\end{matrix}\right)=5$$
$$\text{area}\space OBC=\frac{1}{2}|{\mathbf{b}}\times{\mathbf{c}}|=\frac{\sqrt{50}}{2}=\frac{5\sqrt{2}}{2}$$
$$\text{volume}\space OABC=\left|\frac{1}{6}{\mathbf{a}}\bullet({\mathbf{b}}\times{\mathbf{c}})\right|=\frac{5}{6}$$


## Lines
The equation of a line using vectors.
![[Pasted image 20221003113923.png]]
$$L:r={\mathbf{a}}+\lambda{\mathbf{b}}$$
Where:
- $L$ is the line.
- ${\mathbf{a}}$ is a position vector that is on the line.
- ${\mathbf{b}}$ is a direction vector that is the direction of the line.
- $\lambda$ is a scalar.

Given that, ${\mathbf{r}}-{\mathbf{a}}$ must be parallel to ${\mathbf{b}}$.

We have an implicit equation, $({\mathbf{r}}-{\mathbf{a}})\times{\mathbf{b}}=0$.

**Example 1**

The points $A$, $B$ and $C$ have position vectors $\left(\begin{matrix}1\\3\\2\end{matrix}\right)$, $\left(\begin{matrix}-1\\0\\1\end{matrix}\right)$ and $\left(\begin{matrix}2\\1\\0\end{matrix}\right)$

Find a vector equation of the straight line $AB$.
$$({\mathbf{r}}-{\mathbf{a}})\times{\mathbf{b}}$$
$$\left({\mathbf{r}}-\left(\begin{matrix}1\\3\\2\end{matrix}\right)\right)\times\left(\begin{matrix}-2\\-3\\-1\end{matrix}\right)=0$$

Find a cartesian form of the equation of the straight line $AB$.

$$\left(\left(\begin{matrix}x\\y\\z\end{matrix}\right)-\left(\begin{matrix}1\\3\\2\end{matrix}\right)\right)\times\left(\begin{matrix}-2\\-3\\-1\end{matrix}\right)=0$$
${\mathbf{r}}-{\mathbf{a}}$ is parallel to ${\mathbf{b}}$, therefore, one is a multiple of the other, say $\lambda$ times bigger.
$$\left(\begin{matrix}x-1\\y-3\\z-2\end{matrix}\right)=\lambda\left(\begin{matrix}-2\\-3\\-1\end{matrix}\right)$$
$$x-1=-2\lambda$$
$$y-3=-3\lambda$$
$$z-2=-\lambda$$
$$\implies \frac{1-x}{2}=\frac{3-y}{3}=2-z=\lambda$$

Calculate the [[Vector#Lines#Shortest Distance to Line|shortest distance]] of $C$ to the line.
$$\frac{\left|\left(\begin{matrix}-1\\2\\2\end{matrix}\right)\times\left(\begin{matrix}-2\\-3\\-1\end{matrix}\right)\right|}{\left|\left(\begin{matrix}-2\\-3\\-1\end{matrix}\right)\right|}=\frac{\sqrt{90}}{\sqrt{14}}\approx2.5$$

### Applications
#### Shortest Distance to Line
Given a line with position vector ${\mathbf{a}}$ and direction vector ${\mathbf{b}}$, the shortest distance between point ${\mathbf{c}}$ and the line is:
$$\frac{|({\mathbf{a}}-{\mathbf{c}})\times{\mathbf{b}}|}{|{\mathbf{b}}|}=\left||{\mathbf{a}}-{\mathbf{c}}|\sin\theta\right|=\text{dist}$$

##### Derivation
![[Pasted image 20221003124011.png]]
The shortest distance $\text{dist}=|{\mathbf{a}}-{\mathbf{c}}|\sin\theta$
That is because the distance will be perpendicular, therefore, we have a right-angle triangle.

We find $\sin\theta$ by the cross-product of $({\mathbf{a}}-{\mathbf{c}})\times{\mathbf{b}}$ which yields $|{\mathbf{a}}-{\mathbf{c}}||{\mathbf{b}}|\sin\theta \hat{\mathbf{n}}$.

To eliminate $\hat{\mathbf{n}}$, we take the modulus of both sides.

$$|({\mathbf{a}}-{\mathbf{c}})\times{\mathbf{b}}|=\left||{\mathbf{a}}-{\mathbf{c}}||{\mathbf{b}}|\sin\theta\right|$$
$$\implies\frac{|({\mathbf{a}}-{\mathbf{c}})\times{\mathbf{b}}|}{|{\mathbf{b}}|}=\left||{\mathbf{a}}-{\mathbf{c}}|\sin\theta\right|=\text{dist}$$

#### Shortest Distance Between Two Skew Lines
![[Pasted image 20221003130312.png]]
Let $XY$ be the shortest distance. The line $XY$ is perpendicular to both lines, thus ${\mathbf{b}}\times{\mathbf{d}}$ gives its direction. The unit vector of this direction would be:
$$\frac{{\mathbf{b}}\times{\mathbf{d}}}{|{\mathbf{b}}\times{\mathbf{d}}|}$$
#Todo fix this over right arrow.
$$\overrightarrow{QP}={\mathbf{a}}-{\mathbf{c}}+\lambda{\mathbf{b}}-\mu{\mathbf{d}}$$ 
We can find the length of $QP$ after it's projected onto $XY$.
$$|\overrightarrow{XY}|=({\mathbf{a}}-{\mathbf{c}}+\lambda{\mathbf{b}}-\mu{\mathbf{d}})\bullet\frac{{\mathbf{b}}\times{\mathbf{d}}}{|{\mathbf{b}}\times{\mathbf{d}}|}$$
Because, ${\mathbf{b}}\bullet({\mathbf{b}}\times{\mathbf{d}})=0$ and ${\mathbf{d}}\bullet({\mathbf{b}}\times{\mathbf{d}})=0$, and because we want distance to be positive:
$$|\vec{XY}|=\left|\frac{({\mathbf{a}}-{\mathbf{c}})\bullet({\mathbf{b}}\times{\mathbf{d}})}{|{\mathbf{b}}\times{\mathbf{d}}|}\right|$$
## Planes
We can write the equation of a plane using vectors:
$$\Pi:r={\mathbf{a}}+\lambda{\mathbf{b}}+\mu{\mathbf{c}}$$
Where:
- $\Pi$ is the plane.
- $r$ is any general point on the plane.
- $\mathbf{a}$ is a position vector on the plane.
- $\lambda$ and $\mu$ are scalar variables.
- $\mathbf{b}$ and $\mathbf{c}$ are direction vectors and are not parallel.

We can also write the equation of a plane implicitly:
$${\mathbf{r}}\bullet{\mathbf{n}}={\mathbf{a}}\bullet{\mathbf{n}}$$

Where:
- ${\mathbf{r}}$ is any general point on the plane.
- ${\mathbf{a}}$ is a position vector on the plane.
- ${\mathbf{n}}$ is a direction vector that is normal to the plane.

> [!Tip]
> You can define ${\mathbf{n}}$ in terms of ${\mathbf{b}}$ and ${\mathbf{c}}$.
> $${\mathbf{n}}={\mathbf{b}}\times{\mathbf{c}}$$

This yields:
$${\mathbf{r}}\bullet({\mathbf{b}}\times{\mathbf{c}})={\mathbf{a}}\bullet({\mathbf{b}}\times{\mathbf{c}})$$

This can be converted into cartesian form by defining ${\mathbf{r}}$ as $\left(\begin{matrix}x\\y\\z\end{matrix}\right)$ and then calculating the [[Vector#Triple Scalar Product#Definition|triple scalar product]].

**Example 1**

 A plane passes through the points $A(2,2,-1)$, $B(3,2,-1)$ and $C(4,3,5)$. Write the plane equation in cartesian form and vector form.

$${\mathbf{d_1}}={\mathbf{A}}-{\mathbf{B}}=\left(\begin{matrix}-1\\0\\0\end{matrix}\right)$$
$${\mathbf{d_2}}={\mathbf{C}}-{\mathbf{A}}=\left(\begin{matrix}2\\1\\6\end{matrix}\right)$$

$$\left(\begin{matrix}x\\y\\z\end{matrix}\right)\bullet({\mathbf{d_1}}\times{\mathbf d_2})=\vec{C}\bullet({\mathbf{d_1}}\times{\mathbf d_2})$$
$$\text{det}\left[\begin{matrix}x&y&z\\-1&0&0\\2&1&6\end{matrix}\right]=\text{det}\left[\begin{matrix}4&3&5\\-1&0&0\\2&1&6\end{matrix}\right]$$

$$6y-z=18-5$$
$$6y-z=13$$

### Line of Two Intersecting Planes
![[Pasted image 20221005103715.png#invert_B]]
$$\Pi_1:{\mathbf{r}}\bullet {\mathbf{n_1}}=k_1$$
$$\Pi_2:{\mathbf{r}}\bullet {\mathbf{n_2}}=k_2$$
Given two, non-parallel, planes $\Pi_1$ and $\Pi_2$ such that $\Pi_{1}\neq \Pi_2$. There will always be exactly one line of intersection.

The direction of the line of intersection will be perpendicular to the normals of both planes simultaneously, therefore the direction vector of the line will be equal to:
$${\mathbf{n_1}}\times{\mathbf{n_2}}={\mathbf{d}}$$

To find a point on this line we can reduce the planes to 2 lines and find a point of intersection.

The two planes are reduced to lines by taking a variable and setting it to zero.

$$l_1=\Pi_{1}|_{x=0}$$
$$l_2=\Pi_{2}|_{x=0}$$

The point, ${\mathbf{a}}$, of intersection of $l_1$ and $l_2$ is found when solving the equation:
$$l_1=l_2$$

The point $\mathbf{a}$ will have an $x$ component of zero.

Therefore, the line of intersection will yield the equation
$$l:r={\mathbf{a}}+\lambda{\mathbf{d}}$$

**Example 1**
Find the equation of the line of intersection of the planes $\Pi_1$ and $\Pi_2$ where:
$$\Pi_{1}:{\mathbf{r}}\bullet\left(\begin{matrix}2\\-2\\-1\end{matrix}\right)=5$$
$$\Pi_{2}:{\mathbf{r}}\bullet\left(\begin{matrix}1\\-3\\1\end{matrix}\right)=2$$

Firstly, to find the direction vector of the line, take the cross product of the normal vectors of both planes.

$${\mathbf{d}}=\left(\begin{matrix}2\\-2\\-1\end{matrix}\right)\times\left(\begin{matrix}1\\-3\\1\end{matrix}\right)=\text{det}\left[\begin{matrix}i&j&k\\2&-2&-1\\1&-3&1\end{matrix}\right]=\left(\begin{matrix}-5\\-3\\-4\end{matrix}\right)$$

Secondly, to find a point on the plane, the planes must be reduced to lines by setting one of their variables to a constant (of which, zero is the simplest to work with).

$$\Pi_1:2x-2y-z=5$$
$$\Pi_2:x-3y+z=2$$

In this case, the solving process is most simplified by setting the $y$ variables to zero.

$$l_1=\Pi_{1}|_{y=0}$$
$$l_2=\Pi_{2}|_{y=0}$$

$$\therefore$$

$$2x-z=5$$
$$x+z=2$$
$$\space$$
$$3x=7\implies x=\frac{7}{3}$$
$$\implies z=2-\frac{7}{3}=-\frac{1}{3}$$
$$y=0$$

Thus,

$${\mathbf{a}}=\left(\begin{matrix}\frac{7}{3}\\0\\-\frac{1}{3}\end{matrix}\right)$$

Finally, the equation of the line of intersection is:
$${\mathbf{r}}=\left(\begin{matrix}\frac{7}{3}\\0\\-\frac{1}{3}\end{matrix}\right)+\lambda\left(\begin{matrix}5\\3\\4\end{matrix}\right)$$

### Angle Between Two Planes

The angle between two planes is found by rearranging the [[Vector#Scalar Dot Product|scalar product]] of the two normals. 

$${\mathbf{n_1}}\bullet{\mathbf{n_2}}=\cos\theta |{\mathbf{n_1}}||{\mathbf{n_2}}|$$
$$\implies\theta=\arccos\left(\frac{{\mathbf{n_1}}\bullet{\mathbf{n_2}}}{|{\mathbf{n_1}}||{\mathbf{n_2}}|}\right)$$

This can be seen by taking the cross section of the planes through the line of intersection and then using *trivial* geometry.

> [!Warning]
> Taking the cross product of both normals of both planes is inadvisable because it is unknown whether the resultant angle is obtuse of acute.