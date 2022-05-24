#Quadratics #Polynomials #Maths 

[^1]: $x \in \mathbb{C}$ means $x$ is an element of the set of [[Complex Numbers|complex numbers]].
[^2]: [[Complex Numbers#Imaginary Numbers|Imaginary numbers]]
[^3]: $x^0=1$
# Solving Quadratic Equations by Factorization 
![[factorized_quadratic.png#invert_B]]
Any quadratic equation, $ax^2 + bx + c$, can be factorized as long as $x \in \mathbb{C}$[^1]. However, if $x \notin \mathbb{R}$, then quadratic equations such as $x^2 + 2 = 0$ are not factorable. A factorized form of $x^2+2$ is $(x-i\sqrt{2})(x+i\sqrt{2})$ where $i$ is an imaginary number[^2]

## Method
Say you are given a quadratic equation $$x^2 - 2x + 1 = 0$$![[factorized_quadratic_1.png#invert_B|540]]Where the coefficients of $x^2$, $x^1$ and $x^0$[^3] are $a=1$, $b=-2$ and $c=1$ respectively. 

### Splitting the Middle Term
A method called 'splitting the middle term' can be used.
It involves rewriting the middle term, $bx$, as a sum of two $x$ terms such that the equation can be 'grouped' into two factorable terms.

Let me explain.
The term $-2x$  can be rewritten as $-x -x$. Therefore, the equation can be rewritten as $x^2 -x -x + 1 = 0$. Now, the equation can be 'grouped' into two terms $x^2-x$ and $-x + 1$ which are both factorable.

$$x^2-x = x(x-1)$$and
$$-x+1 = (-1)(x-1)$$Penultimately, the equation can be expressed as $$x(x-1) + (-1)(x-1)=0$$Notice that the this equation is now in the form $xk + (-1)k$ which can be factorized: $k(x-1)$.

This means that the equation $x^2 -2x+1=0$ can be factorized and take the form $$(x-1)(x-1)=0$$ or $$(x-1)^2=0$$
Let's try a more difficult problem and attempt to generalize it! 
Let us factorize $$3x^2+10x+8 = 0$$$3$, $10$ and $8$ have no common factor (except $1$ which wouldn't help), therefore, we should split the middle term $10$ so that the new four terms form two factorable 'groups'.
A way of doing this is by finding two numbers $j$ and $k$ such that $$j \times k = 3 \times 8 = a \times b$$ and $$j + k = 10 = b$$i.e., two numbers who's sum is $10$ and product is $24$. Or, to put it in general terms. Find two numbers that sum to the coefficient of $x^1$ and multiply to give the product of the coefficients of $x^2$ and $x^0$.

In this case: $$6 \times 4 = 24$$ and $$6 + 4 = 10$$ therefore $j=6$ and $k=4$.

Now let's rewrite the middle term $10x$ with $j$ and $k$. $$3x^2 + 6x + 4x + 8 = 0$$ $$(3x^2 + 6x) + (4x + 8) = 0$$ Now factorize the two groups.
$$3x^2 + 6x = 3x(x+2)$$
$$4x+8=4(x+2)$$
so,
$$3x^2+6x+4x+8=3x(x+2)+4(x+2)=(3x+4)(x+2)$$
Finally, $$(3x+4)(x+2)=0$$
### Solving
Now that we have a quadratic equation in the factorized form $$(3x+4)(x+2) = 0$$We have to find the values of $x$ that satisfy this equation. There are two terms being multiplied. The product of the two terms is zero if one or both of the terms equal to zero. This means that the equation is satisfied when $$3x+4=0$$ or when $$x+2=0$$
Consequently, we can solve both of these equations to solve for $x$.
$$x=-\frac{4}{3},\space x=-2$$$-\frac{4}{3}$ and $-2$ are the **[[Solving Quadratic Equations#Roots|roots]]** of the quadratic equation.