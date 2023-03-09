# Statistics
## Continuous Uniform Distributions
### Variance of a Uniform Distribution
Where $X \sim U(a,b)$
$$\text{Var}(X)=\frac{(b-a)^2}{12}$$ 
### Expected value of a Uniform Distribution
Where $X \sim U(a,b)$
$$E(X)=\frac{a+b}{2}$$

### Variance
$$\text{Var}(X)=\frac{S_{xx}}{n}$$
$$\text{Covar}(x,y)=\frac{S_{xy}}{n}$$
$$S_{\alpha\beta}=\sum(\alpha\beta)-\frac{\sum(\alpha) \times \sum(\beta)}{n}$$

If $\alpha$ and $\beta$ are independent, then the combined variance of $\sigma_\alpha$ and $\sigma_\beta$
$$\sigma_c^2=\frac{n_\alpha\times\sigma_\alpha^2+n_\beta\times\sigma_\beta^2}{n_\alpha+n_\beta}$$
$$S_c^2=\frac{(n_\alpha-1) S_\alpha^2+(n_\beta-1)S_\beta^2}{n_\alpha+n_\beta-2}=\frac{S_{\alpha\alpha}+S_{\beta\beta}}{n_\alpha+n_\beta-2}$$

### T-test for two samples
$$T=\frac{\overline{X}-\overline{Y}-(\mu_X-\mu_Y)}{S_c\sqrt{\frac1{n_X}+\frac{1}{n_Y}}}$$