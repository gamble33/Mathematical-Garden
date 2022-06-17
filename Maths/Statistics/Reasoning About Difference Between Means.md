#Statistics #Maths 

# Reasoning About Difference Between Means
---
$\overline{X}$ is roughly [[Normal Distribution|normally]] distributed as the [[Sample|size]] becomes large.

If 
$$\overline{X}\sim N\left(\mu_x, \frac{\sigma_x^2}{n}\right)$$
and
$$\overline{Y} \sim N \left( \mu_y, \frac{\sigma_y^2}{n} \right)$$
then ( #Todo link this to combining random variables)
$$\overline{X}-\overline{Y} \sim N\left(\mu_x-\mu_y, \frac{\sigma_x^2}{n}+\frac{\sigma_y^2}{n} \right)$$
therefore,
$$Z=\frac{(\overline{X}-\overline{Y})-(\mu_x-\mu_y)}{\sqrt{\frac{\sigma_x^2}{n}+\frac{\sigma_y^2}{n}}}$$

## Test for difference between to means
If 
$$X \sim N(\mu_x, \sigma_x^2)$$
and the independent variable $$Y \sim N(\mu_y, \sigma^2_n)$$
then, a test of the null hypothesis $H_0: \mu_x=\mu_y$ can be carried out using the test statistic

$$Z=\frac{(\overline{X}-\overline{Y})-(\mu_x-\mu_y)}{\sqrt{\frac{\sigma_x^2}{n}+\frac{\sigma_y^2}{n}}}$$