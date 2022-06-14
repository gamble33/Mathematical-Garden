#CompSci 

# Pointer Data Type
---
A pointer [[Variable|variable]] is one that stores the reference to a memory location.

## Code Examples
Cambridge's Pseudocode defines pointer variable definition as 
```FORTRAN
IntegerValue <- 5
TIntegerPointer <- ^IntegerValue
```
[[Dereferencing]] a pointer in Cambridge's Pseudocode is defined as
```FORTRAN
IntegerValue2 <- TIntegerPointer^
PRINT IntegerValue2 = IntegerValue ! Outputs: TRUE
```

C defines a pointer definition as
```C
int i = 5;
int i_pointer = &i;
```