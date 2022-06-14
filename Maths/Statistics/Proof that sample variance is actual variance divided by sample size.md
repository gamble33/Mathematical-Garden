#Statistics #Maths

# Proof that $$Var(\overline{X})=\frac{\sigma^2}{n}$$
---
#Todo link variance extracting to combining random variables.

A [[Random Sample|random sample]] $X_1, X_2, ..., X_n$ is taken from a [[Population|population]] where $X\sim N(\mu, \sigma^2)$.
$$\overline{X}=\frac{1}{n}(X_1+X_2+...+X_n)$$
$$\text{Var}(\overline{X})=\text{Var}\left( \frac{1}{n}(X_1+X_2+...+X_n) \right)$$
$$=\frac{1}{n^2}\text{Var}\left( X_1+X_2+...+X_n \right)$$
$$=\frac{1}{n^2}\left(\text{Var}( X_1)+\text{Var}(X_2)+...+\text{Var}(X_n) \right)$$
By definition, $\text{Var}(X)=\sigma^2$.
$$\text{Var}(\overline{X})=\frac{1}{n^2}(n\sigma^2)$$
$$=\frac{n\sigma^2}{n^2}=\frac{\sigma^2}{n}$$