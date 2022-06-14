#Project #CompSci

# Depseudofication Project
---

## Analysis
### Problem

## Cambridge Pseudocode Grammar
Declaring a [[Pointer|pointer]]:
```FORTRAN
TYPE
TIntegerPointer <- ^INTEGER
```
Assigning the [[Memory Address|memory address]] of a value to a pointer:
```FORTRAN
DECLARE IntVar : INTEGER

IntVar <- 57
IntPointer <- @IntVar
```

[[Dereferencing]] a pointer:
```FORTRAN
IntPointer^ 
! Evaluates to the value stored at the memory location
! that IntPointer is pointing to.
```