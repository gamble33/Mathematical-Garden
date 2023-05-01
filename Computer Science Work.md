# Reverse Polish Notations
Expressions can be expressed in:
- Postfix ($3\ 4\ +$)
- Infix ($3+4$)
- Prefix($+\ 3\ 4$)

Reverse Polish Notation is postfix.

It emulates the process in which values are evaluated on a stack.

E.g., for the following RPN expression: 
$$3\ 4\ +\ 2\ \times\ 1\ +$$

The stack state will look like the following, with each column being a different state of the stack.

|     | 4   |     | 2   |     | 1   |     |
| --- | --- | --- | --- | --- | --- | --- |
| 3   | 3   | 7   | 7   | 14  | 14  | 15  | 

# Boolean Algebra
## Basics
Any value or [[Variable|variable]] in Boolean algebra is either $1$ (true) or $0$ (false).
**Example operations**
$$1+1=1$$
$$1+0=1$$
$$0+0=0$$
$$1.0=0$$
## Laws
### Identity
$$1.A=A$$
$$0+A=A$$
### Null
$$0.A=0$$
$$1+A=1$$
### Idempotent
$$A.A=A$$
$$A+A=A$$
### Inverse
$$A.{\overline A}=0$$
$$A+{\overline A}=1$$
### Commutative
$$A.B=B.A$$
$$A+B=B+A$$
### Associative
$$(A.B).C=A.(B.C)$$
$$(A+B)+C=A+(B+C)$$
### Distributive
$$A+B.C=(A+B).(A+C)$$
$$A.(B+C)=A.B+A.C$$
### Absorption
$$A.(A+B)=A$$
$$A+A.B=A$$
### De Morgan's
$${\overline {A.B}} = {\overline A} + {\overline{B}}$$
$$\overline{A+B}=\overline{A}.\overline{B}$$
### Double Complement
$$\overline{\overline{A}}=A$$