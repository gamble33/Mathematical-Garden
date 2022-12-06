#Maths

# MAT Questions
## 2022, Q2
![[Pasted image 20221013104012.png]]
![[Pasted image 20221013104027.png]]
$$\ln{(1-0.5)}=\ln(0.5)=-\ln({2})$$
If we allow $x$ to equal $\frac{1}{2}$, then we have the following result.
$$\ln({1-\frac{1}{2}})=-\frac{1}{2}-\frac{(\frac{1}{2})^2}{2}-\frac{(\frac{1}{2})^3}{3}-\dots$$
$$\ln(1-\frac 1 2)=-\ln2$$
$$\implies-\ln2=-\frac{1}{2}-\frac{(\frac{1}{2})^2}{2}-\frac{(\frac{1}{2})^3}{3}-\dots$$
$$\implies\ln2=\frac{1}{2}+\frac{(\frac{1}{2})^2}{2}+\frac{(\frac{1}{2})^3}{3}+\dots$$
$$=\frac{1}{2}+\frac{1}{2\times2^2}+\frac{1}{3\times2^3}+\dots$$
![[Pasted image 20221013105052.png]]
$$\frac k{24} < \frac{1}{2}+\frac{1}{2\times2^2}+\frac{1}{3\times2^{3}}+\dots<\frac{k+1}{24}$$
$$k < 12+\frac{24}{2\times2^2}+\frac{24}{3\times2^{3}}+\frac{24}{4\times2^{4}}+\frac{24}{5\times2^{5}}+\frac{24}{6\times2^{6}}\dots<{k+1}$$
$$k < 12+3+1+\dots<{k+1}$$
$$k=16$$

![[Pasted image 20221013113932.png]]
$x<0$ because of the alternating sign pattern.
$$\ln\frac 3 2=\ln[1-(-0.5)]$$
$$x=-0.5$$
$$\ln{\frac 3 2}=\ln[1-(-0.5)]=\frac 1 2 - \frac{(-\frac 1 2)^2}{2}-\frac{(-\frac 1 2)^3}{3}-\frac{(-\frac 1 2)^4}{4}-\frac{(-\frac 1 2)^5}{5}-\dots$$
$$=\frac 1 2 - \frac{1}{2\times2^2}+\frac{1}{3\times2^3}-\frac{1}{4\times2^4}+\frac{1}{5\times2^5}-\dots$$
$$\ln{\frac 3 2}+\ln2=\ln3$$
$$\implies \ln3=\left[\frac 1 2 - \frac{1}{2\times2^2}+\frac{1}{3\times2^3}-\frac{1}{4\times2^4}+\frac{1}{5\times2^5}-\dots\right]+\left[\frac{1}{2}+\frac{1}{2\times2^2}+\frac{1}{3\times2^3}+\frac{1}{4\times2^4}+\frac{1}{5\times2^5}+\dots\right]$$
Every second term in both sequences cancel out with the other sequence.
The alternate are equal and are therefore result in the double.
$$\implies\ln3=1+\frac{2}{3\times2^3}+\frac{2}{5\times2^5}+\dots$$
$$=1+\frac{1}{3\times2^2}+\frac{1}{5\times2^4}+\dots$$
$$=1+\sum\limits^\infty_{n=1}\frac{1}{(2n+1)\times2^{2n}}$$
![[Pasted image 20221013115628.png]]
$$1+\frac1 {12} + \frac 1 {80} + \frac{1}{448}+\dots$$
$$1+\frac{1}{12}+A$$
Given that $A>0$,
$$\frac{13}{12}<1+\frac{1}{12}+A$$
$$\frac{13}{12}<\frac{13}{12}+A$$
Therefore, the lower bound of $\ln3$ is $\frac{13}{12}$.

$$\frac{1}{(2n+1)\times2^{2n}}<\frac{1}{5\times2^{2n}}\space\text{for}\space n>2$$
$$1+\frac{1}{3\times2^2}+\frac{1}{5\times2^4}+\frac{1}{7\times2^6}+\dots<1+\frac1{3\times2^2}+\frac{1}{5\times2^4}+\frac{1}{5\times2^6}+\dots$$
$$B=1+\frac1{12}+\frac{1}{5\times2^4}\left[1+\frac{1}{2^2}+\frac{1}{2^4}+\frac{1}{2^6}+\dots\right]$$
Consider $B\times10$,
$$B\times10=10+\frac{10}{12}+\frac{10}{5\times2^4}\left[1+\frac{1}{2^2}+\frac{1}{2^4}+\frac{1}{2^6}+\dots\right]$$
$$\left[1+\frac{1}{2^2}+\frac{1}{2^4}+\frac{1}{2^6}+\dots\right]=G_n=1\times\left(\frac{1}{4}\right)^{n-1}$$
$$\therefore S_n=\frac{1}{1-\frac{1}{4}}=\frac{1}{\frac{3}{4}}=\frac{4}{3}$$
$$\therefore \left[1+\frac{1}{2^2}+\frac{1}{2^4}+\frac{1}{2^6}+\dots\right]=\frac{4}{3}$$
$$B\times10=10+\frac{10}{12}+\frac{10}{5\times2^4}\times\frac{4}{3}$$
$$=10+\frac{10}{12}+\frac{1}{6}=11$$
$$B=\frac{11}{10}$$
Because,
$$1+\frac{1}{3\times2^2}+\frac{1}{5\times2^4}+\frac{1}{7\times2^6}+\dots<1+\frac1{3\times2^2}+\frac{1}{5\times2^4}+\frac{1}{5\times2^6}+\dots$$
$$1+\frac{1}{3\times2^2}+\frac{1}{5\times2^4}+\frac{1}{7\times2^6}+\dots<\frac{11}{10}$$
$$\ln3<\frac{11}{10}$$
Combining the results above, we have that
$$\frac{13}{12}<\ln3<\frac{11}{10}$$

![[Pasted image 20221013124748.png]]
$$3^{17}>4^{13}$$
$$3^{17}>(2^2)^{13}$$
$$3^{17}>2^{26}$$
Take natural logarithms (base $e$) of both sides. This is permissible because $\frac{d}{dx}\left(\ln{x}\right)>0$.
$$\ln{3^{17}}>\ln{2^{26}}$$
$$17\ln3>26\ln2$$

The bounds of $17\ln3$ are:
$$\left(\frac{13\times17}{12},\frac{11\times17}{10}\right)=\left(\frac{26\times17}{24},\frac{11\times17}{10}\right)$$
The bounds of $26\ln2$ are:
$$\left(\frac{16\times26}{24},\frac{17\times26}{24}\right)$$
The lower bound of $17\ln3$ is equal to the upper bound of $26\ln2$. Therefore,
$$17\ln3>26\ln2$$
$$\therefore 3^{17}>4^{13}$$
## 2020 Q2
![[Pasted image 20221017152842.png]]
![[Pasted image 20221017154545.png]]
$$100=2^6+2^5+2^2$$
$$100=gfgf(1)$$

$g(n)$ shifts the binary number to the left, twice.
$f(n)$ shifts the binary number to the left, once, and adds $0001_2$.

![[Pasted image 20221017154610.png]]
$200$ in binary is $11001000_2$ or $2^7+2^6+2^3$
Starting with a $0001_2$. $fgf(1)$ can be applied to obtain $00011001_2$, however there is no combination of $f$ and $g$ that will append three $0$'s to the number without adding any $1$'s. In other words, there is no combination of these functions that is the equivalent of a bit-shift(3) operation `n << 3`.

![[Pasted image 20221017154625.png]]
Every number in $\mathcal{S}$ will have $x$ 1 bits. The only way to increase the amount of bits in the binary number is to apply $f(n)$. To obtain a number with $x$ bits, $f(n)$ should be applied $x-1$ times (because the starting number is $0001_2$ which already contains 1 bit).

![[Pasted image 20221017160231.png]]
$$n\in\mathcal{S}$$
Basis: Let $k=1$,
$$2^{1} \leq n \lt 2^{2}$$
$$\therefore n\neq0, n=1 \implies u_1=1$$
Let $k=2$,
$$2^{2}\leq n \lt 2^3$$
$$n=0100_2=4$$
$$n=0111_2=7$$
$$u_2=2$$
Let $k=3$,
$$2^{3}\leq n \lt 2^4$$
$n \neq 1000_2$
$n = 1001_2$
$n \neq 1010_2$
$n \neq 1011_2$
$n = 1100_2$
$n \neq 1101_2$
$n \neq 1110_2$
$n = 1111_2$
$$u_{3}=3$$
## 2020 Q5
![[Pasted image 20221017163033.png]]
$$\text{Miriam max}=15S \space 15R: \sum\limits^{15}_{r=1}r+15^2$$
$$=\frac{15}{2}(15+1)+15^2=120+15^{2}=345\space\text{sweets}$$
$$\text{Miriam min}=15R \space 15S:0\times15 + \sum\limits^{15}_{r=1}{r}$$
$$=120 \space \text{sweets}$$

![[Pasted image 20221017163753.png]]
$$15R \space 15S: \sum\limits^{15}_{k=1}{k}=120\space\text{sweets}$$
$$15S\space15R:\sum\limits^{30}_{k=16}{k}$$
$$=\sum\limits^{30}_{k=1}{k}-\sum\limits^{15}_{k=1}{k}=15(31)-120=23\times15=345$$


![[Pasted image 20221017164612.png]]
By swapping around an adjacent sunny and rainy day, Miriam's and Adam's total sweet intake is incremented by 1.

On the $k^{\text{th}}$ day that is rainy,
- Miriam consumes $m$ sweets. 
	- Where $m$ is the number of sunny days that there have been during the holiday so far.
- Adam consumes $k$ sweets.

On the $(k+1)^{\text{th}}$ day that is sunny,
- Miriam consumes $m+1$ sweets.
- Adam consumes $0$ sweets.

On the $k^{\text{th}}$ day that is sunny,
- Miriam consumes $m+1$ sweets. 
- Adam consumes $0$ sweets.

On the $(k+1)^{\text{th}}$ day that is rainy,
- Miriam consumes $m+1$ sweets.
- Adam consumes $k+1$ sweets.

The amount of sweets consumed up until the $k^{\text{th}}$ day remains unchanged.

The amount of sweets consumed after the $(k+1)^{\text{th}}$ day also remains the same.

Therefore the difference in sweet consumption for Miriam, by swapping a rainy and a sunny day, is $(m)+(m+1)-[(m+1)+(m+1)]=1$

The difference in sweet consumption for Adam, by swapping a rainy and sunny day is $0+k-(k+1)-0=1$.

![[Pasted image 20221017170001.png]]
Yes.

15r. 15s

## 2021 Q5
![[Pasted image 20221017171753.png]]
![[Pasted image 20221017171804.png]]

![[Pasted image 20221017172419.png]]
$$f(3)=1$$
$$f(4)=0$$
$$f(5)=3$$
$$f(6)=1$$
$$f(7)=\{\begin{matrix}(3,3,1)_3&((3,2,2))_3\end{matrix}\}$$

If $(a,b,c)$ is a triangular triple, then
- $b+c \gt a$
- $a+c \gt b$
- $a+b \gt c$
Therefore for, $(a+1,b+1,c+1)$, the following inequalities must remain true. This is because the sum of any two components was greater than the third. Now the sum of any two components must be greater than the third minus one. Which will still be satisfied.
- $b+c+2>a+1$ $\implies b+c > a - 1$
- $a+c+2>b+1 \implies a + c > b-1$
- $a+b+2>c+1 \implies a + b > c-1$
