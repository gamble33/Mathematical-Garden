```ad-notation
A function, $f(x)$, with a superscript $n$ refers to the $n^{\text{th}}$ derivative of $f(x)$.

i.e.,
$$f^{(m)}(x)\equiv\frac{d^m\left[f(x)\right]}{dx^m}$$
$$f^{(0)}(x)\equiv f(x)$$

The following notation will also be used:
$$f'(x)\equiv\frac{d\left[f(x)\right]}{dx}$$
```

$$\frac{d^n}{dx^n}f(x)g(x)=\sum^n_{k=0}\left(\begin{matrix}n\\k\end{matrix}\right)f^{(n-k)}(x)g^{(k)}(x)$$

Basis
---
First, a proof from first principles that $\frac{d}{dx}f(x)g(x)\equiv f'(x)g(x)+f(x)g'(x)$.
$$\frac{d}{dx}f(x)g(x)\equiv\lim_{h \to 0}\left[\frac{f(x+h)g(x+h)-f(x)g(x)}{(x+h)-x}\right]$$
$$\equiv\lim_{h \to 0}\left[\frac{f(x+h)g(x+h)-f(x)g(x)}{h}\right]$$

next, add and subtract either $f(x+h)g(x)$ or $f(x)g(x+h)$. Both will work, I decided to use $f(x+h)g(x)$.

$$
\equiv\lim_{h \to 0}\left[\frac
{f(x+h)g(x+h)-f(x)g(x)+f(x+h)g(x)-f(x+h)g(x)}
{h}\right]
$$

$$
\equiv\lim_{h \to 0}\left[\frac
{f(x+h)\left[g(x+h)-g(x)\right]+g(x)\left[f(x+h)-f(x)\right]}
{h}\right]
$$

as limits behave linearly, the fraction can be split into multiple terms (I'm not actually sure of the proof of the linearity of taking limits #Todo). 

$$
\equiv\lim_{h \to 0}\left[f(x+h)\frac
{g(x+h)-g(x)}
{h}\right]
+
\lim_{h \to 0}\left[g(x)\frac
{f(x+h)-f(x)}
{h}\right]
$$

again, because of the linearity of limits, the following manipulation is valid.

$$
\equiv
\lim_{h \to 0}\left[f(x+h)\right]

\times\lim_{h \to 0}\left[\frac
{g(x+h)-g(x)}
{h}\right]
+

\lim_{h \to 0}\left[g(x)\right]
\times
\lim_{h \to 0}\left[\frac
{f(x+h)-f(x)}
{h}\right]
$$

by definition, $\frac{d\left[f(x)\right]}{dx}\equiv\lim_{h\to0}\left[\frac{f(x+h)-f(x)}{h}\right]$

$$
\implies
\frac{d}{dx}f(x)g(x) \equiv
f(x)g'(x)+f'(x)g(x)
$$

For $n=1$,

$$\frac{d}{dx}f(x)g(x)=\sum^1_{k=0}\left(\begin{matrix}1\\k\end{matrix}\right)f^{(1-k)}(x)g^{(k)}(x)$$

$$=
\left(\begin{matrix}1\\0\end{matrix}\right)f^{(1)}(x)g^{(0)}(x) +
\left(\begin{matrix}1\\1\end{matrix}\right)f^{(0)}(x)g^{(1)}(x)
$$

$$=f'(x)g(x) + f(x)g'(x)$$

Assumption
---
Assume for $n=\lambda$,

$$\frac{d^\lambda}{dx^\lambda}f(x)g(x)=\sum^\lambda_{k=0}\left(\begin{matrix}\lambda\\k\end{matrix}\right)f^{(\lambda-k)}(x)g^{(k)}(x)$$

Induction
---
Consider $n=\lambda + 1$,

$$
\frac{d^{\lambda + 1}}{dx^{\lambda + 1}}f(x)g(x)
\equiv
\frac{d}{dx}\left[
\frac{d^{\lambda}}{dx^{\lambda}}f(x)g(x)
\right]
$$

$$
\equiv
\frac{d}{dx}\left[
\sum^\lambda_{k=0}\left(\begin{matrix}\lambda\\k\end{matrix}\right)f^{(\lambda-k)}(x)g^{(k)}(x)
\right]
$$

by the linearity of derivatives,

$$
\equiv
\sum^\lambda_{k=0}
\left(\begin{matrix}\lambda\\k\end{matrix}\right)
\frac{d}{dx}\left[f^{(\lambda-k)}(x)g^{(k)}(x)\right]
$$

let $h_1(x)=f^{(\lambda-k)}$, let $h_2(x)=g^{(k)}(x)$
$$\therefore$$

$$
\sum^\lambda_{k=0}
\left(\begin{matrix}\lambda\\k\end{matrix}\right)
\frac{d}{dx}\left[h_1(x)h_2(x)\right]

\equiv

\sum^\lambda_{k=0}\left[
\left(\begin{matrix}\lambda\\k\end{matrix}\right)
h_1'(x)h_2(x)+h_1(x)h_2'(x)
\right]
$$

$$
\equiv

\sum^\lambda_{k=0}
\left(\begin{matrix}\lambda\\k\end{matrix}\right)
\left[
f^{((\lambda + 1) - k)}(x)g^{(k)}(x)+f^{(\lambda-k)}g^{(k+1)}(x)
\right]
$$

$$
\equiv

\sum^\lambda_{k=0}
\left(\begin{matrix}\lambda\\k\end{matrix}\right)
f^{((\lambda + 1) - k)}(x)g^{(k)}(x)
+
\sum^\lambda_{k=0}
\left(\begin{matrix}\lambda\\k\end{matrix}\right)
f^{(\lambda-k)}g^{(k+1)}(x)
$$

```ad-info
Here, the upper limit of the sum is incremented by $1$ $(\lambda + 1)$ and so is the starting point $(k+1)$.

If you consider a sum: 
$$\sum^{3}_{i=1}i=1+2+3=6$$

It is equivalent to say:
$$(2-1) + (3-1) + (4-1) = 6$$

therefore,
$$\sum^{3+1}_{i={1+1}}(i-1)=6$$

to generalize,

$$\sum^n_{i=k}i\equiv\sum^{n+1}_{i={k+1}}(i-1)$$

This applies to derivatives too.

$$\sum^n_{i=k}f^{(i)}(x)\equiv\sum^{n+1}_{i={k+1}}f^{(i-1)}(x)$$

this is the logic being applied below.

Hopefully that was usefull in case you missed the step. It's not complicated but I was stuck on this step idk.
```

$$
\equiv

\sum^{\lambda}_{k=0}
\left(\begin{matrix}\lambda\\k\end{matrix}\right)
f^{(\lambda - k + 1)}(x)g^{(k)}(x)
+
\sum^{\lambda+1}_{k=1}
\left(\begin{matrix}\lambda\\k-1\end{matrix}\right)
f^{(\lambda-k+1)}g^{(k)}(x)
$$

$$
\equiv


\left(

\left[
\sum^{\lambda}_{k=1}
\left(\begin{matrix}\lambda\\k\end{matrix}\right)
f^{(\lambda - k + 1)}(x)g^{(k)}(x)
\right]

+

f^{(\lambda+1)}g(x)
\right)

+

\left(

\left[
\sum^{\lambda}_{k=1}
\left(\begin{matrix}\lambda\\k-1\end{matrix}\right)
f^{(\lambda-k+1)}g^{(k)}(x)
\right]
+

f(x)g^{(\lambda+1)}

\right)
$$

$$
\equiv

f^{(\lambda+1)}g(x) + f(x)g^{(\lambda+1)}

+

\sum^{\lambda}_{k=1}
\left(\begin{matrix}\lambda\\k\end{matrix}\right)
f^{(\lambda - k + 1)}(x)g^{(k)}(x)

+

\sum^{\lambda}_{k=1}
\left(\begin{matrix}\lambda\\k-1\end{matrix}\right)
f^{(\lambda-k+1)}g^{(k)}(x)

$$

$$
\equiv

f^{(\lambda+1)}g(x) + f(x)g^{(\lambda+1)}

+

\sum^{\lambda}_{k=1}
f^{(\lambda - k + 1)}(x)g^{(k)}(x) \left [
\left(\begin{matrix}\lambda\\k\end{matrix}\right) +
\left(\begin{matrix}\lambda\\k-1\end{matrix}\right)
\right]
$$

```ad-info
$$
\left(\begin{matrix}\lambda\\k\end{matrix}\right) +
\left(\begin{matrix}\lambda\\k-1\end{matrix}\right)
\equiv
\frac{\lambda!}{k!(\lambda-k)!}+\frac{\lambda!}{(k-1)!(\lambda-k+1)!}
$$

$$\equiv\frac
{\lambda!(k-1)!(\lambda-k+1)!+\lambda!k!(\lambda-k)!}
{k!(\lambda-k)!(k-1)!(\lambda-k+1)!}
$$

$$\equiv\frac
{\lambda!(k-1)!(\lambda-k+1)+\lambda!k!}
{k!(k-1)!(\lambda-k+1)!}
$$

$$\equiv\frac
{\lambda!k!(\lambda-k+1)\frac1k+\lambda!k!}
{k!(k-1)!(\lambda-k+1)!}
$$

$$\equiv\frac
{\lambda!(\lambda-k+1)\frac1k+\lambda!}
{(k-1)!(\lambda-k+1)!}
$$

$$\equiv\frac
{\lambda!(\frac{\lambda}{k}-1+1+\frac1k)}
{(k-1)!((\lambda+1)-k)!}
$$

$$\equiv\frac
{\lambda!(\frac{\lambda}{k}+\frac1k)}
{(k-1)!((\lambda+1)-k)!}
$$

$$\equiv\frac
{\lambda!(\frac{\lambda+1}{k})}
{(k-1)!((\lambda+1)-k)!}
$$

$$\equiv\frac
{(\lambda+1)!}
{k(k-1)!((\lambda+1)-k)!}
$$

$$\equiv\frac
{(\lambda+1)!}
{k!((\lambda+1)-k)!}
$$

$$\therefore 
\left(\begin{matrix}\lambda\\k\end{matrix}\right) +
\left(\begin{matrix}\lambda\\k-1\end{matrix}\right)
\equiv
\left(\begin{matrix}\lambda+1\\k\end{matrix}\right) 
```

$$
\equiv

f^{(\lambda+1)}g(x) + f(x)g^{(\lambda+1)}

+

\sum^{\lambda}_{k=1}
f^{(\lambda - k + 1)}(x)g^{(k)}(x) \left [
\left(\begin{matrix}\lambda+1\\k\end{matrix}\right)
\right]
$$

the terms outside of the summation are both the ($k=0$) and ($k=\lambda + 1$) terms of the summation that follows, respectively.

$$
\equiv

\left(\begin{matrix}\lambda+1\\0\end{matrix}\right)
f^{(\lambda+1)}g(x) 

+ 

\left(\begin{matrix}\lambda+1\\0\end{matrix}\right)
f(x)g^{(\lambda+1)}

+

\sum^{\lambda}_{k=1}
f^{(\lambda - k + 1)}(x)g^{(k)}(x) \left [
\left(\begin{matrix}\lambda+1\\k\end{matrix}\right)
\right]
$$

$$
\equiv

\sum^{\lambda+1}_{k=0}
\left(\begin{matrix}\lambda+1\\k\end{matrix}\right)
f^{((\lambda+1) - k)}(x)g^{(k)}(x)
$$

Conclusion:
---
If the statement is true for $n=\lambda$, then it must be true for $n=\lambda+1$. Since the statement is true for $n=1$, it must be true $\forall n \geq 1$.
