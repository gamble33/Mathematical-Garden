# Definitions
```ad-definition
A **statistic** is a value based on a sample.
```

```ad-definition
A **parameter** is a value based on a population.
```

```ad-definition
The probability distribution of $T$ is the description how the statistic $T$ can vary based on the sample. We call this the **sampling distribution of a statistic**
```

> [!Example]
> A large bar contains counters. $60\%$ of the counters have the number $0$ on them and $40\%$ have the number $1$.
> 
> > [!question] 
> > a) Find the mean, $\mu$, and the variance, $\sigma^2$, for this population of counters.
> > > [!answer]
> > > > [!note]
> > > > Both $\mu$ and $\sigma^2$ are parameters because they are descriptions of a population.
> > >
> > > $$\mu=0.6\times0+0.4\times1=0.4$$ 
> > > \
> > > $$\sigma^2=0.6\times0^2+0.4\times1^2-0.4^2$$
> > > $$=0.4-0.4^2$$
> > > $$=0.24$$
> 
> A simple random sample of size $3$ is taken from this population.
> 
> > [!question] 
> > b)  List all possible samples.
> > > [!answer]
> > > $$\{0,0,0\}$$
> > > $$\{0,0,1\}$$
> > > $$\{0,1,1\}$$
> > > $$\{1,1,1\}$$
> 
> > [!question]
> > c) Find the sampling distribution for the mean:
> > $$\overline{X}=\frac{X_1+X_2+X_3}{3}$$
> > where $X_1$, $X_2$, and $X_3$ are the three variables representing counters within the sample.
> > 
> > > [!answer]
> > > | $x$                   | $$0$$     | $$\frac13$$ | $$\frac23$$ | $$1$$     |
> > >| --------------------- | --------- | ----------- | ----------- | --------- |
> > > | $$P(\overline{X}=x)$$ | $$0.216$$ | $$0.432$$   | $$0.288$$   | $$0.064$$ |
>
> 
> > [!question]
> > d) Hence, find $E(\overline{X})$ and $\text{Var}(\overline{X})$.
> > > [!answer]
> > > $$E(\overline{X})=0.4$$ 
> > > $$\text{Var}(\overline{X})=0.08$$
> 
> > [!question]
> > e) Find the sampling distribution for the mode $M$.
> > > [!answer]
> > > | $$x$$                           | $0$       | $1$       |
> > >| ------------------------------- | --------- | --------- |
> > >| $$P({M}=x)$$ | $$0.648$$ | $$0.352$$ | 
> 
> > [!question]
> > f) Hence, find $E(M)$ and $\text{Var}(M)$.
> > $$E(M)=0.352$$
> > $$\text{Var}(M)=0.228$$
>
> Parameters:
> * The **population** had a **mean** ($\mu$) of $0.4$
> * The **population** had a **variance** ($\sigma^2$) of $0.24$
> * The **population** had a **mode**  of $0$
>
> Statistics:
> * The **sample** has an expected sample **mean** ($E(\overline{X})$) of $0.4$
> * The **sample** has a mean with **variance**, $\text{Var}(\overline{X})$, of $0.08$
> * The **sample** has an expected sample **mode** , $E(M)$, of $0.352$
>
> Observations:
> * The expected sample mean is equal to the population mean. (It's a good estimate)
> * The expected sample mode has no clear relation to the population mode (it's a bad estimate)
> * The variance of the sample mean is related to the population variance and therefore it's a **biased estimator**.


