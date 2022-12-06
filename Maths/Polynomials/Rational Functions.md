#Polynomials #Maths 

# [[Rational Numbers|Rational]] [[Functions]]
---
Functions that are expressible as the fraction of two [[Polynomials|polynomials]].

The [[Roots of Polynomials|roots]] of the denominator will yield the location of any vertical [[Asymptotes|asymptotes]].

## Finding Vertical Asymptotes
**Example 1**
$$y=\frac{2x-3}{x^2-2x-8}$$
By finding the roots of the denominator,
$$x^2-2x-8=0$$
$$(x-4)(x+2)=0$$
$$\implies \text{vertical asymptotes at} \space x=4,\space x=-2$$
**Example 2**
$$y=\frac{x^2+2x}{x^2-4}$$
Sometimes, simplifying the fraction is required.
By factorizing the numerator and denominator we get
$$y=\frac{x(x+2)}{(x+2)(x-2)}$$
The $(x+2)$ terms cancel out.
$$y=\frac{x}{x-2}$$
Therefore, we know the only vertical asymptote is at $x=2$.
## Finding Horizontal Asymptotes
When the denominator is of an equal order to the numerator, then there will be a horizontal asymptote at $y=k$ where $k$ is some constant. When the denominator is of a greater order, the horizontal asymptote will be at $y=0$.

## Finding [[Turning Points]]
### By [[Differentiation]]
$$y=\frac{3x+2}{(x+2)(x+1)}$$
By using [[Quotient Rule|quotient rule]] we find the [[Derivative|derivative]]
$$\frac{dy}{dx}=\frac{[3][x+2[x+1]-[3x+2][2x+4]}{(x+2)^2(x+1)^2}$$
The derivative is equal to zero only when the numerator is zero, therefore:
$$-3x^2-9x=0$$
$$T_p: x=0,\space x=-3$$
**Example 2**
$$y=\frac{x-2}{(x-3)(x-1)}$$
$$[x-2]'=1$$
$$(x-3)(x-1)=x^2-4x+3 \implies \left[(x-3)(x-1)\right]'=2x-4$$
$$\frac{dy}{dx}=\frac{(x-3)(x-1)-(2x-4)(x-2)}{(x-3)^2(x-1)^2}$$
$$x^2-4x+3-2x^2+4x+4x-8=0$$
$$x^2-4x+5=0$$
$$x=\frac{4 \pm \sqrt{-4}}{2}$$
$$x=2 \pm i$$
$$\implies \text{The curve}\space y \space \text{has no turning points.}$$
### By Algebraic Manipulation
Step 1: Rearrange into a quadratic in terms of $x$.
**Example 1**
$$y=\frac{(x+5)^2}{(x-3)(x-4)}$$
Step 1: Rearrange into a quadratic in terms of $x$.
$$y(x-3)(x-4)=(x+5)^2$$
$$yx^2-7xy+12y=x^2+10x+25$$
$$(y-1)x^2+(-7y-10)x+(12y-25)=0$$
Step 2: Assume $b^2-4ac<0$.
$$(-7y-10)^2-4(y-1)(12y-25)<0$$
$$49y^2+140y+100-4(12y^2-25y-12y+25)<0$$
$$49y^2+140y+100-48y^2+100y+48y-100<0$$
$$y^2+288y<0$$
$$y(y+288)<0$$
$$-288<y<0$$
Within that region $y$ can not exist. Therefore, those limits imply boundary points.