#Statistics #Maths 

# Normal Distribution Function Derivation
---
Imagine a scenario in which arrows are being shot at a target.
![[target.png#invert_B|400]]
A few assumptions must be made about this scenario.
## Assumptions

^e3137a

1. The probability densities of the orthogonal directions are [[Independence|independent]]. The error in the x-direction does not affect  the error in the y-direction.
2. Hitting the centre of the target is more likely than other points on the target. I.e., The centre of the target is being aimed at.
3. The probability density is **rotationally invariant**, meaning, the distribution of where the arrow lands only depends on the distance of the arrow to the centre.

The position of any arrow on the target can be described as a cartesian coordinate $(x, y)$.

![[target_axes.png#invert_B|500]]

The probability of hitting any point on the target $\mathbb{P}(x,y)$ is equal to $\mathbb{P}(x)\times \mathbb{P}(y)$ because of [[Normal Distribution Function Derivation#Assumptions|assumption 1]].

#Todo Area on a arrow target diagram

The probability of hitting any area on the arrow target is equal to $\mathbb{P}(x)dx \times \mathbb{P}(y)dy$. The probability of hitting. The probability of hitting any point on the arrow target can also be represented as $g(r)$ where $r$ is the radius from the centre. Any point that is a distance $r$ from the centre will have the same probability as per [[Normal Distribution Function Derivation#Assumptions|assumption 3]].

#Todo 
$g(r)=\mathbb{P}(x) \times \mathbb{P}(y)$.
Differentiate with respect to $\theta$. 
$\frac{g(r)}{d\theta} = \frac{d}{d\theta}[\mathbb{P}(x)\times\mathbb{P}(y)]$.
$\frac{dg(r)}{d\theta} = \frac{d\mathbb{P}(y)}{d\theta}\mathbb{P}(x) + \frac{d\mathbb{P}(x)}{d\theta}\mathbb{P}(y)$.

#Todo Draw a diagram explaining: given a coordinate $(x,y)$,
$x = r\cos{\theta}$.
$y=r\sin{\theta}.$
$\frac{dx}{d\theta}=-r\sin{\theta}$.
$\frac{dy}{d\theta}=r\cos{\theta}$.
$\frac{dx}{d\theta}=-y$.
$\frac{dy}{d\theta}=x$.

$\frac{dg(r)}{d\theta} = \frac{d\mathbb{P}(y)}{d\theta}\mathbb{P}(x)\times\frac{dy}{dy} + \frac{d\mathbb{P}(x)}{d\theta}\mathbb{P}(y)\times\frac{dx}{dx}$.


$\frac{dg(r)}{d\theta} = \frac{d\mathbb{P}(y)}{dy}\mathbb{P}(x)\times\frac{dy}{d\theta} + \frac{d\mathbb{P}(x)}{dx}\mathbb{P}(y)\times\frac{dx}{\theta}$.


$\frac{dg(r)}{d\theta} = \frac{d\mathbb{P}(y)}{dy}\mathbb{P}(x)x - \frac{d\mathbb{P}(x)}{dx}\mathbb{P}(y)y$ .

$d\theta$ is independent of $dg(r)$ therefore, $\frac{dg(r)}{d\theta} = 0$.

#Todo Fix up constants (make them different)

If two independent variables are equal to each other, then they must be equal to some constant $C$.

$\frac{d\mathbb{P}(x)}{dx}\mathbb{P}(y)y=\frac{\mathbb{P}(y)}{dy}\mathbb{P}(x)x=C$.

$\mathbb{P}'(x)\mathbb{P}(y)y=\mathbb{P}'y\mathbb{P}(x)x=C$.

$\frac{\mathbb{P}(y)y}{\mathbb{P}'(y)}=\frac{\mathbb{P}(x)x}{\mathbb{P}'(x)}$.

let $N$ be some constant.
$\frac{\mathbb{P}(x)x}{\mathbb{P}'(x)}=N$.

$\frac{\mathbb{P}'(x)}{\mathbb{P}(x)x}=C$.

$\frac{\mathbb{P}'(x)}{\mathbb{P}(x)}=Cx$.

$\int{\frac{\mathbb{P}'(x)}{\mathbb{P}(x)}}dx=\int{Cx}{dx}$.

$\ln{|\mathbb{P}(x)|}=\frac{C}{2}x^2+C$.

$e^{\ln{|\mathbb{P}(x)|}}=e^{\frac{C}{2}x^2+C}$.


$\mathbb{P}(x)=e^{\frac{C}{2}x^2}\times e^{C}$. #Todo Why is $e^{ln{|x|}}=x$ and not $|x|$?

let $e^{C}=A$.

$\mathbb{P}(x)=Ae^{\frac{C}{2}x^2}$.