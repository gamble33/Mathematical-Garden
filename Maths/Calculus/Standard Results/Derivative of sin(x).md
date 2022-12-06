#Calculus #Maths 

# [[Derivative]] of $\sin{x}$
---
$$\frac{d\left( \sin{x} \right)}{dx}=\cos{x}$$
## Derivation from [[First Principles|first principles]]
By definition of the derivative:
$$f'(x)=\lim_{k \to 0}{ \frac{f(x+k)-f(x)}{k} }$$
Thus, with $f(x)=\sin{x}$,
$$\frac{d\left( \sin{x} \right)}{dx}=\lim_{k \to 0}{ \frac{\sin(x+k)-\sin{x}}{k} }$$
By using the [[Sin Compound Angle Formula|sin compound angle formula]], we obtain
$$=\lim_{k \to 0}{ \frac{\sin{x}\cos{k}+\sin{k}\cos{x}-\sin{x}}{k} }$$

$$=\lim_{k \to 0}{ \frac{\sin{x}(\cos{k}-1)+\sin{k}\cos{x}}{k} }$$

$$=\lim_{k \to 0}{ \left[ \frac{\sin{x}(\cos{k}-1)}{k}+\frac{\sin{k}\cos{x}}{k} \right] }$$

$$=\lim_{k \to 0}{ \frac{\sin{x}(\cos{k}-1)}{k} } + \lim_{k \to 0}{ \frac{\sin{k}\cos{x}}{k} }$$
By using the [[Limits#Linearity|linearity of the operation of taking a limit]], we can extract $\sin{x}$ and $\cos{x}$.

$$=\sin{x}\lim_{k \to 0}{ \frac{\cos{k}-1}{k} } + \cos{x}\lim_{k \to 0}{ \frac{\sin{k}}{k} }$$
By relying on the following [[Standard Limits|standard limits]]
- $\lim_{k \to 0}{\frac{\sin{k}}{k}}=1$
- $\lim_{k \to 0}{\frac{\cos{k}-1}{k}}=0$
We can conclude
$$\frac{d \left(\sin{x}\right)}{dx}=\sin{x}\times0+1\times\cos{x}=\cos{x}$$