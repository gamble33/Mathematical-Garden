#CompSci 

[^1]: [`const` keyword in rust](https://doc.rust-lang.org/std/keyword.const.html)

# anastasia
Math library written in Rust.

## Questions
### Use of `#[inline(always)]`
Why should `#[inline(always)]` be used in the context of creating an new vector? Why is it an optimization?
```rust
#[inline(always)]
pub const fn new(x: f32, y: f32, z: f32) -> Self {
  Self { x, y, z }
}
```

### Use of Directories in a Library

![[Pasted image 20220921010922.png]]
So... does `f32.rs` need to exist to use the files within `src/f32/` and why?
a
### `#[cfg(not(target_arch = "spirv"))]` ?
What is this `#[cfg(not(target_arch = "spirv"))]`?

## Development Log
### Day 1
I learnt that bevy uses a math library called glam. I followed glam for a lot of technical (rust-related) steps. I tried to understand how to structure the library well by following their practices. Pretty much recreating glam for many parts.

Created a package called f32 to store 32-bit floating point vectors, matrices, etc. Following the guidance of glam, I decided this package will be the home of the default mathematical structures. Thereafter, I created a file called `vec3.rs` which will contain the implementation of a 3-dimensional vector structure.

```rust
pub struct Vec3 {
  pub x: f32,
  pub y: f32,
  pub z: f32
}
```
I also learnt that creating a function in Rust with the `const` keyword forces the function to be evaluable at compile-time which allows it to be used in static contexts. Here is a helpful explanation:

(`const fn`) marks a function as being callable in the body of a const or static item and in array initializers (commonly called “const contexts”). const fn are restricted in the set of operations they can perform, to ensure that they can be evaluated at compile-time.[^1]

[[anastasia#Use of inline always|A question arose]]. The glam library seemed to use the `#[inline(always)]` tag for the implementation of the `new` function. Why is this the case? 

[[anastasia#Use of Directories in a Library|Another question]].

Added operating overload for adding vectors.
```rust
use core::ops::{Add};

impl Add<Vec3> for Vec3 {
  type Output = Self;

  fn add(self, rhs: Self) -> Self::Output {
    Self {
      x: self.x + rhs.x,
      y: self.y + rhs.y,
      z: self.z + rhs.z,
    }
  }
}
```

Implemented display trait for `Vec3`
```rust
use core::fmt::{Display};

impl Display for Vec3 {
  fn fmt(&self, f: &mut Formatter<'_>) -> std::fmt::Result {
    write!(f, "{{{}, {}, {}}}", self.x, self.y, self.z)
  }
}
```

Implemented other operations.
```rust
#[inline]
pub fn dot(self, rhs: Self) -> f32 {
  (self.x * rhs.x) + (self.y * rhs.y) + (self.z * rhs.z)
}
```