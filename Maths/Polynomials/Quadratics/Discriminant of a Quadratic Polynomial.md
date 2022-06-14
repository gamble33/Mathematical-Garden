#Quadratics #Polynomials #Maths 

# [[Discriminant]] of a Quadratic [[Polynomials|Polynomial]]
---

#Todo make an interactive graph where you can play around with the coefficients $a$, $b$ and $c$ and see how it affects the discriminant and the graph.
![[quadratic_polynomial_discriminant.png#invert_B]]

```jsx:
<projects.graphics.QuizQuestion 
	question={"What is 34 + 35"}
	responses={[
	{ text: "35", correct: false },
	{ text: "36", correct: false },
	{ text: "69", correct: true }
	]}
/>
```

For a quadratic polynomial the discriminant is equal to $b^2-4ac$.

## Assuming that the coefficients $a$, $b$ and $c$ are within the set of all [[Real Numbers|real numbers]]

If the discriminant is equal to zero:
then the quadratic formula can be simplified to $$x=\frac{-b \pm 0}{2a}=\frac{-b}{2a}$$ thus, giving only one distinct, real solution to the equation. The equation plotted as a function of $x$ may look like this:
![[quadratic_1_real_root.png#invert_B]]

If the discriminant is less than zero:
then there are no real solutions (there are only [[Complex Numbers|complex]] solutions because taking a square root of a negative number does not result in a real number) to the equation.  

In other words if $x \in \mathbb{R}$ and $b^2-4ac < 0$  then 
$ax^2 + bx + c \neq 0$

The plot of the function may look like this
![[quadratic_0_real_root.png#invert_B]]

If the discriminant is greater than zero:
then there must be two distinct, real solutions.
![[quadratic_2_real_root.png#invert_B]]