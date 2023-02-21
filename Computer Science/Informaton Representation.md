# Bit Representation
```ad-definition
**Byte**

group of **$8$ bits** treated as a single unit.
```

```ad-definition
**Nibble**

group of **$4$ bits** treated as a single unit.
```

# Binary and Decimal Prefixes
## Decimal Prefixes
| Decimal Prefix Name | Symbol | Factor  |
| ------------------- | ------ | ------- |
| kilo                | $\text{k}$    | $10^3$  |
| mega                | $\text{M}$    | $10^6$  |
| giga                | $\text{G}$    | $10^9$  |
| tera                | $\text{T}$    | $10^12$ |

```ad-failure
In the computing world, decimal prefix names were used to represent what should've been binary prefixes.

$$2^{10}=1024,\space\space\space10^3=1000$$
$$1024 \approx 1000$$
So computer scientists referred to **$N\ \text{gigabytes}$** as **$N\times2^{20}\ \text{bytes}$**.

> [!Example]
> A specification for a computer system may have looked like:
> 
> > Processor Speed: $1.6\ GHz$
> > \
> > Size of RAM: $8\ GB$
> > \
> > Size of hard disk: $400\ GB$
>
> where the $G$ should (mathematically speaking) represent $10^9$, when in reality, almost certainly (actually) represents $2^{20}$

To resolve this unsatisfactory situation, [[Informaton Representation#Binary Prefixes|Binary Prefixes]] were invented.
```

## Binary Prefixes
| Binary Prefix Name | Symbol | Factor   | Factor                |
| ------------------ | ------ | -------- | --------------------- |
| kibi               | $\text{Ki}$   | $2^{10}$ | $1024$                |
| mebi               | $\text{Mi}$   | $2^{20}$ | $1024^2=1048576$      |
| gibi               | $\text{Gi}$   | $2^{30}$ | $1024^3 = 1073741824$ |
| tebi               | $\text{Ti}$   | $2^{40}$ | $1024^4=\dots$        |

```ad-example
Convert $34\ 560\ \text{bytes}$ in to $\text{kibibytes}$.

$$\frac{34560}{2^{10}}=33.75\ \text{KiB}$$
```

```ad-example
Convert $3\ 456\ 000\ \text{bytes}$ in to $\text{mebibytes}$.

$$\frac{3456000}{2^{10}}=3.296\ \text{MiB}$$
```

#ExamTodo Find examples of exam questions for this.

# Coding for Integers
```ad-faq
**Why use two's and one's complement?**

# 1: Less Values
Consider a $4\ \text{bit}$ value $1001$. 

If we were to use a **'sign and magnitude representation'**,

that is, the last three bits would represent the magnitude and the first bit would represent the sign
$$\overbrace{1}^\text{sign}\underbrace{001}_\text{magnitude}$$

Then all the numbers in the set $$[-7,7] \cap \mathbb{Z}$$ could be represented. 
Along with **two representations for zero**:
$$1000 = -0$$
$$0000 = 0$$

| signed denary number | sign and magnitude | two's complement |
| -------------------- | ------------------ | ---------------- |
| $7$                  | $0111$             | $0111$           |
| $1$                  | $0001$             | $0001$           |
| $0$                  | $0000$             | $0000$           |
| $-0$                 | $1000$             | Not represented  |
| $-1$                 | $1001$             | $1111$           |
| $-7$                 | $1111$             | $1001$           |
| $-8$                 | not represented    | $1000$           |

# 2: Less Hardware
If two's complement values are used to represent negative numbers, the same circuitry can be used for subtraction as is used for addition.

> [!Example]
> $6$ in denary is $0110$ in two's complement.
> \
> $-3$ in denary is $1101$ in two's complement.
> $$6 - 3 = 6 + (-3)$$
> $$\implies 0110 + 1101 = 0011$$
> $0011$ is $3$ in two's complement.

#Todo Add further words of intuition as to why this is.
```

