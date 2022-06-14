#CompSci 

# Enumerated Data Type
---
A user-defined, [[Non-Composite Data Type|non-composite data type]] data type for which a value of that type can only be one of a discrete set of possible values. (Confusing explanation. I know.)

## Code Examples
The days of a week is a good example of data type that has a finite amount of possible values.

Cambridge's Pseudocode showcasing two examples of definitions for enumerated data-types.
```fortran
TYPE
TDirections = (North, East, South, West)
TDays = (Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday)
```

Example of a valid enumerated data-type definition in Rust, Java, C++, and many other languages.
```rust
enum Month {
	January,
	February,
	March,
	April,
	May,
	June,
	July,
	August,
	September,
	October,
	November,
	Decembner
}
```