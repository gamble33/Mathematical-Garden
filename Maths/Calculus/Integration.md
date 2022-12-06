# By Substitution
## Boring Version
The goal of the boring version is to simplify a complex-looking expression.

Find an expression, $g(x)$, in the integrand, $\int\limits^a_b{f(g(x))\space dx}$, which is complex-looking. 

Say $u=g(x)$.

Find the new limits $a\prime=g(a)$ and $b\prime=g(b)$.

rearrange 
$$u=g(x) \to x=g^{-1}(u)$$
differentiate with respect to $u$.
$$\frac{dx}{du}=[g^{-1}(u)]'$$
$$dx=du[g^{-1}(u)]'$$

Rewrite the new integral as
$$\int\limits^{a\prime}_{b\prime}{f(u)\times[g^{-1}(u)]' \space du}$$

## *Extreme* Version
The goal of the extreme version is to complexify a simple-looking expression.

Write an expression, $g(u)$ and place it in the integrand, $\int\limits^a_b{f(x)\space dx}$, which is simple-looking. 

Say $x=g(u)$.

Find the new limits $a\prime=g^{-1}(a)$ and $b\prime=g^{-1}(b)$.

differentiate with respect to $u$.
$$\frac{dx}{du}=g'(u)$$
$$dx=du\times g'(u)$$

Rewrite the new integral as
$$\int\limits^{a\prime}_{b\prime}{f(g(u))\times g'(u) \space du}$$

> [!Example]
> $$\int{\frac{1}{1+x^2}dx}=\arctan{x}+C$$
> $$x=\tan{\theta} \to \theta = \arctan{x}$$
> $$\frac{dx}{d\theta} = sec^2{\theta} \to dx=\sec^2{\theta} \space d\theta$$
> $$\implies \therefore \to \int\frac{1}{1+\tan^2{\theta}}\times\sec^2{\theta}\space d\theta$$
> > [!Lalala] 
> > remember: $\tan^2{\theta}+1\equiv\sec^2{\theta}$
>
> $$=\int{\frac{1}{\sec^2{\theta}} \times \sec^2{\theta}\space d\theta}$$
> $$=\int{1 \space d\theta}$$
> $$=\theta=\arctan{x}$$

> [!Example]
> $$\int{\frac 1 {\sqrt{a^2 + x^2}} \space dx}$$
> $$x=a\times\tan{\theta}$$
> $$\frac{dx}{d\theta}=a\times\sec^2\theta\to dx=a\times\sec^2\theta\times d\theta$$
> $$\int{\frac 1 {\sqrt{a^2 + a^2\times\tan^2{\theta}}} \space dx}$$
> $$\int{\frac 1 {\sqrt{a^2(1+\tan^2{\theta})}} \space dx}$$
> $$\int{\frac 1 {a\sqrt{(1+\tan^2{\theta})}} \space dx}$$
> $$\int{\frac 1 {a\sqrt{(\sec^2{\theta})}} \space dx}$$
> $$\int{\frac 1 {a\sqrt{(\sec^2{\theta})}} \times a\times sec^2\theta \space d\theta}$$
> $$\int{\frac 1 {\sec{\theta}} \times sec^2\theta \space d\theta}$$
> $$\int{\frac{1}{\cos\theta}\space d\theta}$$
> $$=\ln{|\sec{\theta}+\tan{\theta}|}+C$$
> $$=\ln{\left|\sqrt{1+\frac{x^2}{a^2}}+\frac{x}{a}\right|}$$
> $$=\text{arsinh}\space{x}+C$$

> [!Example]
> $$\int{\frac{1}{\sqrt{x^2-a^2}}\space dx}$$
> x = sinh($\theta^2%$)
> $$$$
> 