#Maths 

[^1]: [Definition of shear mapping](https://en.wikipedia.org/wiki/Shear_mapping)
[^2]: [[Matrices#Trace]]
[^3]: [[Matrices#Determinant]]

# Matrices
---
## Definitions and Operations
A matrix is an 'array' of numbers.

### Dimensionality
The dimensions of a matrix is its size, in terms of rows and columns
$$\left[ \begin{matrix}
	1 & 3 & -7 \\
	2 & 4 & 1
  \end{matrix} \right]\to \space \text{dimensionality: } 2\times3$$
 If the dimensionality of a matrix is
 - $n\times 1$, it is a column [[Vector|vector]].
 - $1 \times n$, it is a row vector.

#### Square Matrix
A matrix is **square** if it has the same number of rows and columns.

### Minors and Co-factors
For a square matrix, the minor of any element is the determinant of the matrix remaining when the minor and the row and column of the minor are removed.

For a matrix
$${\bf A}=\left[\begin{matrix}a&b&c\\d&e&f\\g&h&i\end{matrix}\right]$$
The minor of $e$ is $\text{det}\left[\begin{matrix}a&c\\g&i\end{matrix}\right]$. I.e., you remove the column and row of the component that you are taking the minor of and form a matrix with the elements that weren't removed. ($\left[\begin{matrix}{\color{green}a}&b&{\color{green}c}\\d&e&f\\{\color{green}g}&h&{\color{green}i}\end{matrix}\right]$)

The co-factor of $a$ is
$$\text{Cofactor}\space{\bf A}_{i,j}=(-1)^{i+j}\times\text{Minor}_{i,j}$$

### Singular
A matrix is singular if it has no inverse.

If $\text{det}\space{\bf A} = |{\bf A}|=0$, then ${\bf A}$ is [[Matrices#Singular|singular]].

### Trace
The trace of a matrix ${\bf A}$ is the sum of the components of the leading diagonal. That is,
$$\text{Trace}({\bf A})\equiv \sum\limits^n_{i=1}a_{(i,i)}$$

### Determinant
The determinant is a calculation made from the values of a matrix. It will determine if a matrix can be inverted.

>[!Note]
>Only a square matrix will have a determinant.

For a $2\times2$ matrix, the determinant is
$$\text{det}\space\left[\begin{matrix}a&b\\c&d\end{matrix}\right]=ad-bc$$

For a $3\times3$ matrix, the determinant is
$$\text{det}\left[\begin{matrix}a&b&c\\d&e&f\\g&h&i\end{matrix}\right]=a\left(\text{det}\left[\begin{matrix}e&f\\h&i\end{matrix}\right]\right)-b\left(\text{det}\left[\begin{matrix}d&f\\g&i\end{matrix}\right]\right)+c\left(\text{det}\left[\begin{matrix}d&e\\g&h\end{matrix}\right]\right)$$
>[!Note]
>This is the product sum of the top row with the co-factors of the top row.

### Augmented Matrix 
The concatenation of two or more matrices. Commonly used for solving simultaneous equations and inversions.

It is typically denoted by:
$$[{\bf A}|{\bf I}]$$
The augmented matrix is frequently used for row operations.

### Zero Matrix
A matrix in which all its elements are $0$.
$${\bf 0}=\left[\begin{matrix} 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{matrix}\right]$$

### Identity Matrix
${\bf I}$ is a square matrix which has $1$'s in the 'leading diagonal' starting from the top left.
$${\bf I}=\left[\begin{matrix}1&0&0\\0&1&0\\0&0&1\end{matrix}\right]$$
$$\bf{A I} = \bf{I A} = \bf{A} \space\text{for all square matrices} \space \bf{A}$$

### Similar Matrices
Two matrices, ${\bf A}$ and ${\bf B}$, are similar if
$${\bf Q A} = {\bf B Q}\space\space\text{and}\space\space\text{det}({\bf Q}) \neq 0$$
then:
$${\bf A}\sim {\bf B}$$
$${\bf A} = {\bf Q}^{-1} {\bf B Q}$$

### Symmetric Matrix
A matrix, $Q$, is symmetric $\text{iff}$ its transpose, $Q^T$, is equal to itself.
$$Q=Q^T$$

### Diagonal Matrix
A matrix where all components are $0$ except the leading diagonal.

> [!Note]
> The leading diagonal can consist of zeros, however, they are not necessary.

> [!Example]
> $$\left[\begin{matrix}1&0&0\\0&9&0\\0&0&14\end{matrix}\right]$$

### Addition and Subtraction
Add the corresponding elements of each matrix. **The dimensionality of the operands must match.**
$$\left[\begin{matrix}
	1 & 3 & -7 \\
	4 & 0 & 5
\end{matrix}\right] + \left[\begin{matrix}
	6 & -2 & 9 \\
	2 & 1 & 0
\end{matrix}\right] = \left[\begin{matrix}
	7 & 1 & 2 \\
	6 & 1 & 5
\end{matrix}\right]$$
### [[Scalar]] Multiplication
$$3\times\left[\begin{matrix}
 1 & 3 & -7 \\ 4 & 0 & 5
\end{matrix}\right] =
\left[\begin{matrix}
 3 & 9 & -21 \\ 12 & 0 & 15
\end{matrix}\right]
$$

### Matrix Multiplication
The sum of the product of each component of a row of the first matrix and each component of the corresponding column of the second matrix is a value in the resultant matrix.
>[!Warning]
> Multiplication of matrices is not [[Commutativity|commutative]]. I.e., ${\bf A B} \neq {\bf B A}$.
 
$${\bf M}={\bf A B}$$
$${\bf A}_\text{dim}=s\times n$$
$${\bf B}_\text{dim}=n\times t$$
$${\bf M}_{p, q}=\sum^n_{r=1}{\bf A}_{p,r}\times{\bf B}_{r,q}$$
**Example Multiplication**
$$ 
\left[
\begin{matrix}
1 & 0 & 3 & -2 \\
2 & 8 & 4 & 3 \\
7 & -1 & 0 & 2
\end{matrix}
\right]
\times
\left[
\begin{matrix}
5 &  1  \\
1 &  7  \\
0 &  3  \\
8 & -3  \\
\end{matrix}
\right]
=
\left[
\begin{matrix}
-11 &  16  \\
42 &  61  \\
50 & -6 
\end{matrix}
\right]
$$
### Inverting
If ${\bf A B}={\bf I}$, then ${\bf A}^{-1}={\bf B}$.
>[!Warning]
>Only square matrices can be inverted.

$$\left[\begin{matrix}a&b\\c&d\end{matrix}\right]\left[\begin{matrix}\alpha&\beta\\\gamma&\delta\end{matrix}\right]=\left[\begin{matrix}1&0\\0&1\end{matrix}\right]$$
$$\therefore$$
$$a\alpha+b\gamma=1,\space a\beta+b\delta=0$$
$$c\alpha+d\gamma=0,\space c\beta+d\delta=1$$

When inverting a matrix, we have two options.
#### The rubbish way (analytical approach)
1. Assume the inverse exists.
2. Calculate the values:
	1. Swap the leading diagonal.
	2. Make the following diagonal negative.
	3. Divide by the determinant.

If
$${\bf A}=\left[\begin{matrix}a&b\\c&d\end{matrix}\right]$$
then,

$${\bf A}^{-1}=\frac{1}{\text{det}({\bf A})}\left[\begin{matrix}d&-b\\-c&a\end{matrix}\right]$$
more generally, it is the matrix of co-factors transposed divided by the determinant (${\bf A}^{-1}=\frac{1}{\text{det}\space{\bf A}}\times{\bf C}^T$).

#### Gauss Jorden Elimination
##### Method to invert $\bf A$
Consider the [[Matrices#Augmented Matrix|augmented matrix]] of $[{\bf A}|{\bf I}]$.

Then use the three row operators:
- Scaling rows: multiply every element in a row by a scalar.
- Permute rows: exchange one row for another.
- Combine rows: adding or subtracting rows from each other.

Turn the $\bf A$ section of the augmented matrix into $\bf I$ (an identity matrix) by using these row operators.
$$[{\bf A}|{\bf I}] \sim [{\bf I}|{\bf A}^{-1}]$$

**Example**
For the inverse of $\left[\begin{matrix}1&3\\4&6\end{matrix}\right]$

Consider the augmented matrix:

$$\left[\begin{matrix}1&3&1&0\\4&6&0&1\end{matrix}\right]$$

Multiply the second row by $\frac{1}{2}$.

$$\left[\begin{matrix}1&3&1&0\\2&3&0&\frac{1}{2}\end{matrix}\right]$$

Subtract the second row from the first.

$$\left[\begin{matrix}-1&0&1&-\frac{1}{2}\\2&3&0&\frac{1}{2}\end{matrix}\right]$$

Add two lots of the first row to the second.

$$\left[\begin{matrix}-1&0&1&-\frac{1}{2}\\0&3&2&-\frac{1}{2}\end{matrix}\right]$$

Multiply the first row by $-1$.

$$\left[\begin{matrix}1&0&-1&\frac{1}{2}\\0&3&2&-\frac{1}{2}\end{matrix}\right]$$

Multiply the second row by $\frac{1}{3}$.

$$\left[\begin{matrix}1&0&-1&\frac{1}{2}\\0&1&\frac{2}{3}&-\frac{1}{6}\end{matrix}\right]$$

$$\implies {\bf A}^{-1}=\left[\begin{matrix}-1&\frac{1}{2}\\\frac{2}{3}&-\frac{1}{6}\end{matrix}\right]$$

### Transposing
${\bf A}^T$ is the transpose of a matrix ${\bf A}$. 

If $a_{i,j}$ is an element of the matrix ${\bf A}$, then ${\bf A}^T$ will have the same value at $a_{j,i}$ (An $m\times n$ matrix becomes $n\times m$). I.e., the rows and columns are interchanged.

**Example**
$$\left[\begin{matrix}1&2&3\\4&5&6\end{matrix}\right]^T=\left[\begin{matrix}1&4\\2&5\\3&6\end{matrix}\right]$$

#### Observations
$$A=\left[\begin{matrix}1&0\\2&-1\\0&3\end{matrix}\right]$$
$$A^T=\left[\begin{matrix}1&2&0\\0&-1&3\end{matrix}\right]$$

$$A^TA=\left[\begin{matrix}5&-2\\-2&10\end{matrix}\right]$$
$$AA^T=\left[\begin{matrix}1&2&0\\2&5&-3\\0&-3&9\end{matrix}\right]$$

A matrix is multipliable by its own transpose

The result will always be square and symmetric.

The multiplication is commutative $\text{iff}$ the original matrix is symmetric.

The [[Matrices#Determinant|determinant]] and [[Matrices#Trace|trace]] are unaffected by a transposition.

$$({\bf AB})^T={\bf B}^T{\bf A}^T$$

## Proofs
If ${\bf P}$ and ${\bf Q}$ are non-singular matrices, prove that $({\bf P Q})^{-1}={\bf Q}^{-1}{\bf P}^{-1}$

Multiply both sides, on the left, by ${\bf Q}$.
$${\bf Q}({\bf P Q})^{-1}={\bf Q}{\bf Q}^{-1}{\bf P}^{-1}={\bf I}{\bf P}^{-1}={\bf P}^{-1}$$

Now multiply both sides, on the left, by ${\bf P}$.
$$\bf{P Q}({\bf P Q})^{-1}={\bf P}{\bf P}^{-1}={\bf I}$$

## Applications to Graphical Transformations

The resultant space of a transformation is known as the **image**.
Object to image.

We use matrices to create a transformation from one space to another. This can be in any dimension. E.g., $\mathbb{R}^2\to\mathbb{R}^2$

### Linear Transformations
If $T$ is a linear transformation, then:
$$T(k{\bf a})=kT({\bf a})$$
$$T({\bf a} + {\bf b}) = T({\bf a}) + T({\bf b})$$
Where:
- ${\bf a}$ is a vector.
- $k$ is a scalar.

We can use an $n\times n$ matrix to create a linear transformation in $n$ dimensional space.

If we have a coordinate $(x,y)$ and apply a transformation matrix, we have the following:
$$\left[\begin{matrix}a&b\\c&d\end{matrix}\right]\left[\begin{matrix}x\\y\end{matrix}\right]=\left[\begin{matrix}ax+by\\cx+dy\end{matrix}\right]$$

Multiplying by a matrix $\left[\begin{matrix}a&b\\c&d\end{matrix}\right]$ represents the mapping ${\bf T}:\left[\begin{matrix}x\\y\end{matrix}\right]\to\left[\begin{matrix}ax+by\\cx+dy\end{matrix}\right]$.

To calculate ${\bf T}$ we can observe what happens to the basis vectors.
> [!Note]
> The basis vectors are the $i$ and $j$ vectors. If we create the augmented matrix of $[i|j]$, we get the identity.

### Invariant Points and Lines
An invariant point is a point that maps to itself.

An invariant line is a line that maps to itself.

> [!Warning]
> An invariant line can be but is not necessarily a collection of invariant points.

### Reflection
To reflect in the y-axis, $i$, $j$ will map to $-i$, $j$.

As a matrix calculation:
$${\bf T}\times[i|j]=[-i|j]$$
$${\bf T}\times{\bf I} = \left[\begin{matrix}-1&0\\0&1\end{matrix}\right]$$
$$\therefore {\bf T}=\left[\begin{matrix}-1&0\\0&1\end{matrix}\right]$$

To reflect in the x-axis, $i$, $j$ will map to $i$, $-j$.

As a matrix calculation:
$${\bf T}\times[i|j]=[i|-j]$$
$${\bf T}\times{\bf I} = \left[\begin{matrix}1&0\\0&-1\end{matrix}\right]$$
$$\therefore {\bf T}=\left[\begin{matrix}1&0\\0&-1\end{matrix}\right]$$

To reflect in the line $y=mx$
$$[i|j] \mapsto \frac{1}{1+m^2}\left[\begin{matrix}1-m^2&2m\\2m&m^2-1\end{matrix}\right]$$
Therefore, the transformation matrix ${\bf T}$ is
$${\bf T} = \frac{1}{1+m^2}\left[\begin{matrix}1-m^2&2m\\2m&m^2-1\end{matrix}\right]$$

Reflection in the line $y=mx$ will always have invariant points that reside on the line $y=mx$. It will also have invariant lines of the form $y=mx$ and $y=-\frac{1}{m}x+c$

### Rotation
 To rotate anticlockwise by $\theta$, 
 $$[i|j] \mapsto \left[\begin{matrix}\cos{\theta}&-\sin{\theta}\\\sin{\theta}&\cos{\theta}\end{matrix}\right]$$
 $$\implies{\bf T}=\left[\begin{matrix}\cos{\theta}&-\sin{\theta}\\\sin{\theta}&\cos{\theta}\end{matrix}\right]$$

Rotation by angle $\theta$ will have no invariant lines and an invariant point at the origin of rotation $(0,0)$. 

### Stretch and Enlargement
To stretch $a$ in the x-axis and $b$ in the y-axis:
$$[i|j]\mapsto \left[\begin{matrix}a&0\\0&b\end{matrix}\right]$$
$$\implies{\bf T}=\left[\begin{matrix}a&0\\0&b\end{matrix}\right]$$
If $a = b$, then ${\bf T}$ is an enlargement.

In the case of enlargement (**but not in the case of a stretch**), every line which passes through the origin will be an invariant line.

In the case of stretching, there are always two invariant lines: $y=0$ and $x=0$.

There is also an invariant point at $(0, 0)$.

### Shear
In plane geometry, a shear mapping is a linear map that displaces each point in a fixed direction, by an amount proportional to its signed distance from the line that is parallel to that direction and goes through the origin.[^1]

#### Shear in the $x$-direction
A shear in the $x$ direction with magnitude $k$ would leave $y$-values unaffected, whilst translating an $x$ value by $ky$.
$${\bf T} \times \left(\begin{matrix}x\\y\end{matrix}\right)=\left(\begin{matrix}x+ky\\y\end{matrix}\right
)$$
$$\therefore {\bf T}=\left[\begin{matrix}1&k\\0&1\end{matrix}\right]$$

#### Shear in the $y$-direction
A shear in the $y$ direction with magnitude $k$ would leave $x$-values unaffected, whilst translating a $y$ value by $kx$.
$${\bf T} \times \left(\begin{matrix}x\\y\end{matrix}\right)=\left(\begin{matrix}x\\y+kx\end{matrix}\right
)$$
$$\therefore {\bf T}=\left[\begin{matrix}1&0\\k&1\end{matrix}\right]$$

The shear transformation only has one line of invariance that is on the axis that you are shearing from.

### Area
The area of an image is equal to the pre-image multiplied by the modulus of the determinant of the transformation matrix.
$$A_2 = |{\text{det}\space{\bf T}}|\times A_1$$

#### Example Exam Question
A stretch and shear matrix is given in the form ${\bf M}=\left[\begin{matrix}s&t\\0&1\end{matrix}\right]$.
Given that the line of invariance for this matrix is $y=5x$ and the scale factor of the area is 3. Find the value of $s$ and $t$.
$$\left[\begin{matrix}s&t\\0&1\end{matrix}\right]\left[\begin{matrix}k\\5k\end{matrix}\right]=\left[\begin{matrix}x'\\y'\end{matrix}\right]$$
$$ks+5kt=x'\implies k=\frac{x'}{s+5t}$$
$$5k=y'\implies k=\frac{y'}{5}$$
$$k=\frac{y'}{5}=k=\frac{x'}{s+5t}$$
$$\implies y'=\frac{5}{s+5t}x'$$
$$5=\frac{5}{s+5t}$$
The scale factor of the area is 3, therefore
$$|\text{det}\space{\bf M}|=3$$
$$\implies (s\times1-t\times0)=s=3$$
$5=\frac{5}{3+5t}$ when $3+5t=1$.
$$t=-\frac{2}{5}$$
$$s=3$$

### Combined Transformations
If you want to transform a matrix $\bf M$ by matrix $\bf A$, followed by matrix $\bf B$. You would use the following calculation:
$$T={\bf B A}$$
$${\bf B A M}={\bf T M}$$
> [!Warning]
> The order of effect is from right to left due to commutativity.

### Inverse Transformations
To inverse a transformation, SIMPLY multiply the image by the inverse of the transformation matrix.

$${\bf T}^{-1}{\bf T M}={\bf T}^{-1}{\bf M}'={\bf M}$$

# Eigenvectors & Eigenvalues
For a given matrix ${\bf A}$, a given eigenvector $x$ and a given eigenvalue $\lambda$, it holds that:
$${\bf A}x = \lambda x$$

- $x$ has to be the same dimension as ${\bf A}$.
- ${\bf A}$ must be a square matrix.

Derived from the definition,
$${\bf Ax} = \lambda {\bf x} = \lambda {\bf I x}$$
$${\bf Ax}-\lambda{\bf I x}=0$$

> [!Note]
> Matrix multiplication is distributive.

$$({\bf A} - \lambda {\bf I}){\bf x}=0$$

> [!Warning]
> Two matrices can multiply to create a [[Matrices#Zero Matrix|zero matrix]]:
>$$\left[\begin{matrix}0&1\\0&1\end{matrix}\right]\left[\begin{matrix}1\\0\end{matrix}\right]=\left[\begin{matrix}0\\0\end{matrix}\right]$$
>Therefore, $({\bf A} - \lambda {\bf I}){\bf x}=0$ can be true without $({\bf A} - \lambda {\bf I})$ being equal to zero.

Multiplying both sides of the equation by $({\bf A} - \lambda {\bf I})^{-1}$ would imply that ${\bf x} = \left(\begin{matrix}0\\0\end{matrix}\right)$, therefore we know that $({\bf A} - \lambda {\bf I})$ is singular.

Therefore, 

$$\text{det}\space(\bf{A} - \lambda {\bf I}) = 0$$

We call this the characteristic equation.

## Characteristic Equation
$$\text{det}\space(\bf{A} - \lambda {\bf I}) = 0$$

The characteristic equation is always a [[Polynomials]] of degree less than or equal to the dimension of the matrix.

Solving the characteristic equation, will yield the eigenvalue, $\lambda$.

As a result of the characteristic equation, the maximum number of distinct eigenvalues (and therefore eigenvectors) is equal to the dimension of the matrix.

## normalised Eigenvector
An eigenvector written as a unit vector.

## Calculating Eigenvectors from a given Eigenvalue
$${\bf A}{\bf x}=\lambda{\bf x}$$
$$({\bf A-\lambda{\bf I}})\left[\begin{matrix}x\\y\\z\\{\vdots}\end{matrix}\right]=\left[\begin{matrix}0\\0\\{\vdots}\end{matrix}\right]$$

Therefore, by multiplying the vector ${\bf x}$ by the matrix ${\bf A} - \lambda {\bf I}$, a set of simultaneous equations can be created to find each component of the vector ${\bf x}$.

Often, a class of solutions is given by the set of simultaneous equations rather than a distinct vector. Thus, values must be chosen from the class of solutions to obtain an eigenvector.

## Properties of Eigenvalues
$$\text{det}({\bf A})\equiv \prod\lambda$$[^2]
$$\text{trace}({\bf A})\equiv \sum\lambda$$[^3]

$$\space$$
$$\text{if}\space{\bf A} \sim \lambda$$
$$\text{then}\space {\bf A}^2 \sim \lambda^2$$
$$\space$$

$$\space$$
$$\text{if}\space{\bf A} \sim \lambda$$
$$\text{then}\space {\bf A}^T \sim \lambda$$
$$\space$$

[[Matrices#Row Operations]]
# Row Operations
![[Pasted image 20221115160327.png]]
(From https://proofwiki.org/wiki/Effect_of_Elementary_Row_Operations_on_Determinant)
#Todo
## Adding Rows
Adding one row to another

# Eigen Decomposition
The process of factorizing a matrix into the product of three matrices comprising a [[Matrices#Diagonal Matrix|diagonal matrix]] and another matrix with its [[Matrices#Inverting|inverse]].

$${\bf A} \equiv {\bf Q \Lambda}{\bf Q}^{-1} $$
where:
- ${\bf Q}$ is the [[Matrices#Augmented Matrix|augmented matrix]] of the [[Matrices#Eigenvectors & Eigenvalues|eigenvectors]] of ${\bf A}$.
- ${\bf \Lambda}$ is the [[Matrices#Diagonal Matrix|diagonal matrix]] whose terms are the [[Matrices#Eigenvectors & Eigenvalues|eigenvalues]] of ${\bf A}$.
	- The ordering of the [[Matrices#Eigenvectors & Eigenvalues|eigenvalues]] are consistent with the ordering of the [[Matrices#Eigenvectors & Eigenvalues|eigenvectors]].

> [!Warning]
> Matrix ${\bf Q}$ must be [[Matrices#Orthogonal Matrix|orthogonal]]. Therefore, the [[Matrices#Eigenvectors & Eigenvalues|eigenvectors]] must also be [[Matrices#Orthogonal Matrix|orthogonal]]. 
> 
> This is because the [[Matrices#Eigenvectors & Eigenvalues|eigenvectors]] cannot be transformed such that all of them are parallel with a distinct coordinate axis if they are not [[Matrices#Orthogonal Matrix|orthogonal]] before any transformations are applied.

> [!Note]
> If the matrix ${\bf A}$ is [[Matrices#Symmetric Matrix|symmetric]], then ${\bf Q}$ must be [[Matrices#Orthogonal Matrix|orthogonal]].

> [!Tip]
> In order for ${\bf \Lambda}$ to have actual [[Matrices#Eigenvectors & Eigenvalues|eigenvalues]], the [[Matrices#Eigenvectors & Eigenvalues|eigenvectors]] that make up ${\bf Q}$ must be normalised.

This has the effect of breaking down the transformation ${\bf A}$ into three separate transformations.

${\bf Q}^{-1}$ has the effect that [[Matrices#Eigenvectors & Eigenvalues|eigenvectors]] are rotated such that they line up the coordinate axes.

${\bf \Lambda}$ has the effect that stretches the space by scale factors $(\lambda_1, \lambda_2, \dots)$ in the direction of the coordinate axes, that is, the direction of the [[Matrices#Eigenvectors & Eigenvalues|eigenvectors]] (as they have been rotated to be parallel to the coordinate axes).

${\bf Q}$ has a rotation effect on the entire space such that the [[Matrices#Eigenvectors & Eigenvalues|eigenvectors]] are now parallel to their original direction again.

## Diagonalising
$${\bf \Lambda} \equiv {\bf Q}^{-1}{\bf A Q}$$

> [!Note]
> ${\bf A}$ and ${\bf \Lambda}$ must be [[Matrices#Similar Matrices|similar]].

> [!Example]
> Diagonalize the matrix ${\bf A}= \left[\begin{matrix}2&-1\\-1&2\end{matrix}\right]$ for form a matrix ${\bf D}$.
> 
> By [[Matrices#Characteristic Equation]]:
> $$\lambda_1 = 1,\space\lambda_2=3$$
> 
> Find normalised [[Matrices#Eigenvectors & Eigenvalues|eigenvectors]]:
> $$\left(\begin{matrix}\frac 1 {\sqrt 2}\\\frac{1}{\sqrt{2}}\end{matrix}\right),\space\left(\begin{matrix}\frac 1 {\sqrt 2}\\-\frac{1}{\sqrt{2}}\end{matrix}\right)$$
> $${\bf D}=\left[\begin{matrix}1&0\\0&3\end{matrix}\right]$$
> $${\bf P}=\left[\begin{matrix}\frac 1 {\sqrt{2}}&\frac{1}{\sqrt{2}}\\\frac{1}{\sqrt{2}}&-\frac{1}{\sqrt{2}}\end{matrix}\right]$$
> Such that ${\bf D}={\bf P}^{-1}{\bf A P}$

### Defective Matrices
Matrices that are not diagonalisable are defective matrices.

The following conditions are the same conditions under which the [[Matrices#Augmented Matrix|augmented matrix]] of [[Matrices#Eigenvectors & Eigenvalues|eigenvectors]] is **not** [[Matrices#Singular|singular]].

There are four conditions under which a matrix is diagonalisable
1. ${\bf eV}_n\neq k\times {\bf eV}_m$

Where:
- $\bf eV$ is an eigenvector of a given matrix.
- $k$ is a scalar multiple.
- $m \neq n$.
- No row of the matrix $\bf P$  can be exclusively zeros. Thus, there must be a non-zero element for every row of at least one [[Matrices#Eigenvectors & Eigenvalues|eigenvector]].

2. There must be the same number of distinct [[Matrices#Eigenvectors & Eigenvalues|eigenvectors/eigenvalues]] as the dimension of the matrix.
3. None of the [[Matrices#Eigenvectors & Eigenvalues|eigenvectors]] can be equal to zero.
4. Every row in the matrix of [[Matrices#Augmented Matrix|augmented]] [[Matrices#Eigenvectors & Eigenvalues|eigenvectors]] must have at least one non-zero element.
	- This is because, by having a row of zeros, the matrix is a projection onto a space of a lower-dimension. Thus, information about that row's direction is lost.
### Applications
#### Finding powers of matrices
$${\bf A}^{n}={\bf P}{\bf D}^n{\bf P}^{-1}$$
$${\bf D}^{n}=\left[\begin{matrix}{\lambda_{1}}^{n}&0&0\\0&{\lambda_{2}}^{n}&0\\0&0&{\lambda_{3}}^{n}\end{matrix}\right]$$

> [!Example]
> $${\bf A}=\left[\begin{matrix}1&2&0\\0&3&1\\0&0&2\end{matrix}\right]$$
> Find ${\bf A}^{16}$.
> $${\bf A} = {\bf P D} {\bf P}^{-1}$$
> Eigenvalues: $\lambda = 1$, $\lambda = 2$, and $\lambda = 3$.
> $$\therefore {\bf D}=\left[\begin{matrix}1&0&0\\0&2&0\\0&0&3\end{matrix}\right]$$
> ${\bf P}$ is the augmented matrix of eigenvectors.
> $${\bf P}=\left[\begin{matrix}1&2&1\\0&1&1\\0&-1&0\end{matrix}\right]$$
> $${\bf A}^{16}={\bf P D P}^{-1}\times{\bf P D P}^{-1}\times\dots\times{\bf P D P}^{-1}$$
> Cancellation occurs (${\bf P}^{-1}{\bf P} = {\bf I}$).
> $${\bf A}^{{16}}={\bf P}{\bf D}^{16}{\bf P}^{-1}$$
> $${\bf D}^{16}=\left[\begin{matrix}1^{16}&0&0\\0&2^{16}&0\\0&0&3^{16}\end{matrix}\right]$$
> $$\vdots$$
> $${\bf A}^{16}=\left[\begin{matrix}1&3^{16-1}&1-2^{17}+3^{16}\\0&3^{16}&3^{16}-2^{16}\\0&0&2^{16}\end{matrix}\right]$$

# Matrix Algebra
## Summation Law
If ${\bf A} = {\bf B} + k {\bf I}$, the [[Matrices#Eigenvectors & Eigenvalues|eigenvectors]] of ${\bf B}$ will match $\bf A$ and the [[Matrices#Eigenvectors & Eigenvalues|eigenvalues]] will be $k$ greater.

### Proof
#### Part $\text{I}$
Proof that [[Matrices#Eigenvectors & Eigenvalues|eigenvectors]] of ${\bf A}$ and $\bf B$ are equal:

Assume for a contradiction that $\bf v$ is not an [[Matrices#Eigenvectors & Eigenvalues|eigenvector]] of $\bf B$ such that ${\bf Bv} \neq \mu {\bf v}$.

However, let $\bf v$ be the eigenvector of ${\bf A}$ such that ${\bf A v} = \lambda {\bf v}$ .
$${\bf A v} = \lambda {\bf v}$$
$$({\bf B} + k {\bf I}){\bf v} = \lambda {\bf v}$$
by the distributive property,
$${\bf B v} + k{\bf I v} = \lambda {\bf v}$$
by the identity principle,
$${\bf B v} + k{\bf v} = \lambda {\bf v}$$
$${\bf B v} = \lambda {\bf v} - k {\bf v}$$
$${\bf B v} = (\lambda - k){\bf v}$$
since both $k$ and $\lambda$ are scalars, let $\mu = \lambda - k$ ,
$${\bf B v} = \mu {\bf v}$$
contradiction.

#### Part $\text{II}$
It follows immediately that the given eigenvalues of $\bf A$ being $\lambda$ and the eigenvalues of $\bf B$ being $\mu$. 
$$\mu = \lambda - k$$
$$\mu + k = \lambda$$
$\lambda$ is $k$ greater than $\mu$.

### General Case
Let $\bf A$ be a matrix with eigenvalue $\lambda$ and corresponding eigenvector $\bf v$.

Let $\bf B$ be a matrix with eigenvalue $\mu$ and corresponding eigenvector $\bf v$.

$$({\bf A} + {\bf B}){\bf v} = {\bf A v} + {\bf B v} = \lambda{\bf v} + \mu{\bf v} = (\lambda + \mu){\bf v}$$

The summation law is one that states what happens to the eigenvalues when matrices which have matching eigenvectors are summed.

## Product Law 
A matrix that is a product of two matrices (which have equal eigenvectors) will have eigenvalues that are the product of the eigenvalues of the factors of the matrix.

Let ${\bf A}$ have an eigenvalue of $\lambda$ with corresponding eigenvector $\bf v$.

Let ${\bf B}$ have an eigenvalue of $\mu$ with corresponding eigenvector $\bf v$.

$$({\bf A B}){\bf v} = {\bf A}({\bf B v})={\bf A}(\mu {\bf v})=\mu(\lambda {\bf v})=\mu\lambda{\bf v}$$

A simple application of associativity.

## Power Law
$${\bf A}^n{\bf v}=\lambda^n{\bf v}$$

A given matrix raised to the power $n$ will have a set of eigenvalues, all raised to the power $n$.

### Not very rigorous proof
$${\bf A}^n{\bf v}={\bf A}^{n-1}({\bf A v})={\bf A}^{n-1}(\lambda {\bf v})={\bf A}^{n-2}{\bf A}(\lambda {\bf v})=\lambda{\bf A}^{n-2}({\bf A}{\bf v})=\lambda^2{\bf A}^{n-2}{\bf v}=\dots=\lambda^n{\bf v}$$

## Cayley-Hamilton Theorem
Consider the [[Matrices#Characteristic Equation|characteristic equation]] of the matrix ${\bf A}$ with eigenvector ${\bf v}$ and eigenvalue $\lambda$.

$$a\lambda^3 + b\lambda^2 + c\lambda + d = 0$$
$$(a\lambda^3 + b\lambda^2 + c\lambda + d){\bf v} = 0{\bf v}$$
$$a\lambda^3{\bf v} + b\lambda^2{\bf v} + c\lambda{\bf v} + d{\bf v} = 0{\bf v}$$
$$a\lambda^3{\bf v} + b\lambda^2{\bf v} + c\lambda{\bf v} = -d{\bf v}$$
$$a{\bf A}^3{\bf v} + b{\bf A}^2{\bf v} + c{\bf A}{\bf v} = -d{\bf Iv}$$
$$(a{\bf A}^3 + b{\bf A}^2 + c{\bf A}){\bf v} = -d{\bf Iv}$$
since $\bf v\neq 0$ , the coefficients must be the same.
$$a{\bf A}^3 + b{\bf A}^2 + c{\bf A} = -d{\bf I}$$
$$(a{\bf A}^2{\bf } + b{\bf A}{\bf } + c{\bf I}){\bf A} = -d{\bf I}$$
$$\frac{a{\bf A}^2+b{\bf A}+c{\bf I}}{-d}={\bf A}^{-1}$$

# Solving Simultaneous Equations with Matrices
If:
$${\bf A}{\bf x} = {\bf v}$$
then,
$${\bf x} = {\bf A}^{-1} {\bf v}$$
where:
- ${\bf x}=\left(\begin{matrix}x\\y\\z\end{matrix}\right)$
- ${\bf A}$ is the coefficient matrix.
- ${\bf v}$ is the solution [[Vector|vector]].

Writing:
$$\left[\begin{matrix}a&b\\c&d\end{matrix}\right]\left[\begin{matrix}x\\y\end{matrix}\right]=\left[\begin{matrix}\alpha\\\beta\end{matrix}\right]$$
is equivalent to:
$$ax+by=\alpha$$
$$cx+dy=\beta$$

> [!Example]
> A colony of $1000$ mole-rats is made up of adult males, adult females and youngsters. Originally, there were $100$ more adult females than adult males.
>
> ![[Pasted image 20221122161103.png]]
> 
> After one year:
> - The number of adult males increased by $2\%$.
> - The number of adult females increased by $3\%$.
> - The number of youngsters had decreased by $4\%$.
> - The total number of mole-rats had decreased by $20$.
> 
> Form and solve a matrix equation to find out how many of each type of mole-rat were in the original colony.
> 
> Let $F_0 = \text{number of female mole-rats originally}$ 
> \
> Let $M_0 = \text{number of male mole-rats originally}$ 
> \
> Let $Y_0 = \text{number of youngsters mole-rats originally}$ 
> 
> Let $F_1 = \text{number of female mole-rats after one year}$ 
> \
> Let $M_1 = \text{number of male mole-rats after one year}$ 
> \
> Let $Y_1 = \text{number of youngsters mole-rats after one year}$ 
>
> converting text into mathematical expressions:
> $$F_0 + M_0 + Y_0=1000$$
> $$F_0 = M_0 + 100$$
> $$M_1 = M_0 \times 1.02$$
> $$F_1 = F_0 \times 1.03$$
> $$Y_1 = Y_0 \times 0.96$$
> $$F_1 + M_1 + Y_1 = 980$$
> \
> rewriting all expressions in terms of $F_0$, $M_0$ and $Y_0$:
> $$F_0 + M_0 + Y_0=1000$$
> $$1.03F_0+1.02M_0+0.96Y_0=980$$
> $$F_0-M_0+0Y_0=100$$
> write the series of simultaneous equations as a matrix:
> $$\left[\begin{matrix}1&1&1\\1.03&1.02&0.96\\1&-1&0\end{matrix}\right]\left[\begin{matrix}F_0\\M_0\\Y_0\end{matrix}\right]=\left[\begin{matrix}1000\\980\\100\end{matrix}\right]$$
> $$\left[\begin{matrix}F_0\\M_0\\Y_0\end{matrix}\right]=\left[\begin{matrix}1&1&1\\1.03&1.02&0.96\\1&-1&0\end{matrix}\right]^{-1}\left[\begin{matrix}1000\\980\\100\end{matrix}\right]$$
> $$\vdots$$
> $$F_0 = 200$$
> $$M_0 = 100$$
> $$Y_0 = 700$$

## Enumerating Solutions
![[Matrices 2022-11-23 10.53.27.excalidraw|1000]]
### Consistency
A system of simultaneous equations is consistent if the equations have any solution. I.e., if it is a solvable set of equations.
### Linear Independence
Two equations are linearly independent if one equation can not be constructed from the other by a series of linear operations.

A system is linearly independent if no equation can be constructed by a linear combination of the others.
### Coefficient Matrix
A non-square coefficient matrix is singular. This could lead to zero of infinite solutions depending on the linear independence. 

### $2D$ Case
![[Pasted image 20221123112241.png]]

### $3D$ Case
**All planes meet at a single point**
- consistent.
- $1$ solution.
![[Pasted image 20221123112932.png]]

**Planes form a sheaf**
- consistent.
- $\infty$ solutions.
![[Pasted image 20221123113000.png]]

**Planes form a prism**
- inconsistent
- $0$ solutions.
![[Pasted image 20221123113116.png]]

**2 or more plane are parallel but non-identical**
- inconsistent
- $0$ solutions.
![[Pasted image 20221123113207.png]]

**Planes are equivalent (co-planar)**
- consistent
- $\infty$ solutions.
![[Pasted image 20221123113240.png]]

### Identifying the Geometric Configuration
$$\text{If}\space {\bf A x} = {\bf B},\space\text{then}\space {\bf A}^*{\bf x}={\bf B}^*$$
$$\text{where}\space \left[{\bf A}^*|{\bf B}^*\right] \space\text{is in augmented reduced row form}$$

Reduced row form is formed with [[Matrices#Row Operations]].
$$\left[\begin{matrix}*&*&*&*\\*&*&*&*\\0&0&\alpha&\beta\end{matrix}\right]$$

$$\text{if}\space\alpha\space\text{is not zero: then there is}\space 1\space\text{solution.}$$
$$\text{if}\space\alpha\space\text{is zero and}\space\beta\space\text{is not zero: then there are no solutions.}$$
$$\text{if}\space\alpha\space\text{is zero and}\space\beta\space\text{is zero: then there is}\space \infty\space\text{solutions.}$$

> [!Example]
> 1.
> 
> $$3x-6z=0$$
> $$3y+3z=2$$
> $$-3x-y+3z=-2$$
> $$\left[\begin{matrix}3&0&-6\\0&3&3\\-3&-1&3\end{matrix}\right]\left[\begin{matrix}x\\y\\z\end{matrix}\right]=\left[\begin{matrix}0\\2\\-2\end{matrix}\right]$$
> The coefficient matrix has a determinant of -18, therefore it can be inverted and a single solution can be found. The geometric configuration of this system of simultaneous equations is a set of planes such that they meet at one point.

> [!Example]
> 2.
> 
> $$3x-y-6z=1$$
> $$x+3y+3z=2$$
> $$-3x-y+3z=-2$$
> $$\left[\begin{matrix}3&-1&-6\\1&3&3\\-3&-1&3\end{matrix}\right]\left[\begin{matrix}x\\y\\z\end{matrix}\right]=\left[\begin{matrix}1\\2\\-2\end{matrix}\right]$$
> The determinant of the coefficient matrix is zero.
> 
> By linear combination of the equations from the set of simultaneous equations:
> $$eq_1+2eq_2:5(x+y)=5$$
> $$eq_1+2eq_3:-3(x+y)=-3$$
> This implies that the solution plane projected onto the $z$-axis is a line.
> 
> Therefore, the solution set in $3$ dimensions is a sheaf.

> [!Example]
> 3.
> 
> $$3x+6y-6z=-6$$
> $$-6x+3y+3z=2$$
> $$-3x-y+3z=-2$$
> $$\left[\begin{matrix}3&6&-6\\-6&3&3\\-3&-1&3\end{matrix}\right]\left[\begin{matrix}x\\y\\z\end{matrix}\right]=\left[\begin{matrix}-6\\2\\-2\end{matrix}\right]$$
> The determinant of the coefficient matrix is zero.
> 
> By linear combination of the equations from the set of simultaneous equations:
> $$eq_1+2eq_2: -9x+12y=-2$$
> $$eq_1+2eq_3:-3x+4x=-10$$
> This implies that the solution plane projected onto the $z$-axis has no solutions. The planes are also not parallel (which can be determined by comparing the normal vectors of the planes, which are not scalar multiples of each other). 
> 
> Therefore, the solution set in $3$ dimensions is a prism.