#Statistics #Maths 

[^1]: [[Expected value is distributive over addition]]
[^2]: [[Expected value is associative over multiplication]]

# Proof that $$E(\overline{X})=\mu$$
---
> [!Note]
> This is a proof that $\overline{X}$ is an [[Unbiased Estimator|unbiased estimator]] for $\mu$ when the population is [[Normal Distribution|normally distributed]].

$$\overline{X}=\frac{1}{n}(X_1+X_2+...+X_n)$$
$$E(\overline{X})=E\left( \frac{1}{n}(X_1+X_2+...+X_n) \right)$$
$$=\frac{1}{n}E\left( (X_1+X_2+...+X_n) \right)$$
$$=\frac{1}{n} \left( E(X_1)+E(X_2)+...+E(X_n) \right)$$
The expected value of one sample unit $E(X_n)$ is equal to $\mu$ (by definition).
$$E(\overline{X})=\frac{1}{n} \left(\mu + ... + \mu \right)$$
$$=\frac{1}{n} (n\mu)=\frac{n\mu}{n}=\mu$$