#Statistics #Maths 

[^1]: [Difference between $2X$ and $X_1 + X_2$](https://www.savemyexams.co.uk/a-level/maths_probability--statistics-2/cie/20/revision-notes/2-statistical-distributions/2-2-linear-combinations-of-random-variables/2-2-1-linear-combinations-of-random-variables/)

# Linear Combination of Random Variables
---
---
> [!Note]
 Variables $X$ and $Y$ must be [[Independence|independent]] for the following to be true.
 
$$E(aX \pm bY)= aE(x) \pm bE(y)$$
$$\text{Var}(aX \pm bY)= a^2\text{Var}(X)+b^2\text{Var}(Y)$$
There is a difference between *one observation* ($2X$) and *two observations* ($X_1 + X_2$)[^1].
![[Pasted image 20220617150256.png]]
## Adding Poisson Distributions
If 
$$X \sim \text{Po}(\lambda_1)$$  and
$$Y \sim \text{Po}(\lambda_2)$$
then
$$(X+Y) \sim \text{Po}(\lambda_1 + \lambda_2)$$